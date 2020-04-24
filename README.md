# LAReQA
[LAReQA](https://arxiv.org/abs/2004.05484) is a recently released, challenging benchmark testing language-agnostic answer retrieval from a multilingual candidate pool. This benchmark involves [...] 

## Data
This directory contains 2 folders corresponding to the XQuAD-R and MLQA-R datasets. 

### XQuAD-R
XQuAD-R is 11-way parallel with 1190 questions per language. [...]
The files are found under the `xquad-r/` folder with the following languages:
* Arabic: `xquad-r/ar.json`
* German: `xquad-r/de.json`
* [...]

### MLQA-R
MLQA-R is not parallel across all languages.
The files are found under the `mlqa-r/` folder with the following languages:
* Arabic: `mlqa-r/ar.json`
* [...]

### Dataset statistics
We show the number of questions and candidate sentences for each language for both data sets in the tables below.

|     | XQuAD-R   |            | MLQA-R    |            |
|-----|-----------|------------|-----------|------------|
|     | questions | candidates | questions | candidates |
| ar  |           |            |           |            |
| de  |           |            |           |            |
| el  |           |            |           |            |
| ... |           |            |           |            |

## Training and Evaluation
We train several baselines models and evaluate them on XQuAD-R and MLQA-R. Our baselines fine-tune [mBERT](INSERT) on retrieval versions of SQuAD v1.1 training data and translations of this data. The trained baselines are released as TFHub modules, linked below for each baseline.

* En-En: 
* X-X:
* X-X-mono:
* X-Y:

In the table below, we show the mean average precision (mAP) of all of our baselines on both datasets.


|          | XQuAD-R | MLQA-R |
|----------|---------|--------|
| En-En    |         |        |
| X-X      |         |        |
| X-X-mono |         |        |
| X-Y      |         |        |


## Reference
If you use this dataset, please cite [[1]](https://arxiv.org/abs/2004.05484):

[1] Roy, U., Constant, N., Al-Rfou, R., Barua, A., Phillips, A., & Yang, Y. (2020). [LAReQA: Language-agnostic answer retrieval from a multilingual pool](https://arxiv.org/abs/2004.05484). arXiv preprint arXiv:2004.05484.
```
@article{roy2020lareqa,
  title={LAReQA: Language-agnostic answer retrieval from a multilingual pool},
  author={Roy, Uma and Constant, Noah and Al-Rfou, Rami and Barua, Aditya and Phillips, Aaron and Yang, Yinfei},
  journal={arXiv preprint arXiv:2004.05484},
  year={2020}
}
```
## License
XQuAD-R is distributed under the [CC BY-SA 4.0 license]().
MLQA-R is distributed under the [insert license]().

This is not an officially supported Google product. 
