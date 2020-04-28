# LAReQA
[LAReQA](https://arxiv.org/abs/2004.05484) is a challenging benchmark testing language-agnostic answer retrieval from a multilingual candidate pool. Unlike previous cross-lingual tasks, LAReQA tests for "strong" cross-lingual alignment, requiring semantically related *cross*-language pairs to be closer in representation space than unrelated *same*-language pairs. As part of the LAReQA benchmark, we construct a QA retrieval task with a multilingual pool by taking an existing cross-lingual *extractive* QA task [XQuAD](https://github.com/deepmind/xquad) and converting it to a *retrieval task*: **XQuAD-R**. We release XQuAD with sentence breaks in this repository for use as XQuAD-R. Section 3.1 of our paper contains more details on how we convert span-tagging tasks into retrieval tasks. Note that files contained in this repository for XQuAD-R are simply the original XQuAD data annotated with sentence boundaries for each of the paragraphs, added as an additional field in the jsons.

## Data
This directory contains 1 folder corresponding to the XQuAD-R datasets.

### XQuAD-R
XQuAD-R is a retrieval version of the XQuAD dataset (a cross-lingual extractive
QA dataset). Like XQuAD, XQUAD-R is an 11-way parallel dataset,  where each
question appears in 11 different languages and has 11 parallel correct answers
across the languages.

The files are found under the `xquad-r/` folder with the following languages:
* Arabic: `xquad-r/ar.json`
* German: `xquad-r/de.json`
* Greek: `xquad-r/el.json`
* English: `xquad-r/en.json`
* Spanish: `xquad-r/es.json`
* Hindi: `xquad-r/hi.json`
* Russian: `xquad-r/ru.json`
* Thai: `xquad-r/th.json`
* Turkish: `xquad-r/tr.json`
* Vietnamese: `xquad-r/vi.json`
* Chinese: `xquad-r/zh.json`

### Dataset statistics
We show the number of questions and candidate sentences for each language for both data sets in the tables below.

|     | XQuAD-R   |            |
|-----|-----------|------------|
|     | questions | candidates |
| ar |      1190 |       1222 |
| de |      1190 |       1276 |
| el |      1190 |       1234 |
| en |      1190 |       1180 |
| es |      1190 |       1215 |
| hi |      1190 |       1244 |
| ru |      1190 |       1219 |
| th |      1190 |        852 |
| tr |      1190 |       1167 |
| vi |      1190 |       1209 |
| zh |      1190 |       1196 |


## Training and Evaluation
We train several baselines models and evaluate them on XQuAD-R and MLQA-R. Our baselines fine-tune [mBERT](https://github.com/google-research/bert) on retrieval versions of [SQuAD v1.1](https://www.aclweb.org/anthology/D16-1264/) training data and translations of this data. See Section 4 of our paper for more details. The trained baselines are released as TFHub modules, linked below for each baseline.

* [En-En]()
* [X-X]()
* [X-X-mono]()
* [X-Y]()

In the table below, we show the mean average precision (mAP) of all of our baselines on both datasets. See Section 5 of our paper for more results.

|          | XQuAD-R |
|----------|---------|
| En-En    |  0.29       |
| X-X      |  0.23       |
| X-X-mono |  0.52       |
| X-Y      |  0.66       |


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
XQuAD-R is distributed under the [CC BY-SA 4.0 license](https://creativecommons.org/licenses/by-sa/4.0/legalcode).

This is not an officially supported Google product.
