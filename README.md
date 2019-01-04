# Analysis on SQuAD 2.0 Submissions

**[SQuAD 2.0](http://stanford-qa.com)** has been a popular benchmark for testing the ability of **Machine Reading Comprehension (MRC)**. In this repository, I will list (almost) all models submitted to SQuAD 2.0 and summarize several features of these models as well as additional development scores. 

Note that, this is an ongoing work and will be updated irregularly.


## Content

| Section | Description |
|-|-|
| [BERT Track](#BERT-Track) | Statistics for BERT-related models |
| [Non-BERT Track](#Non-BERT-Track) | Statistics for non-BERT-related models |
| [Ensemble Track](#Ensemble-Track) | Statistics for ensemble models |
| [BERT-TF and BERT-PT](#BERT-TF-and-BERT-PT) | Comparisons on TensorFlow & PyTorch version of BERT |
| [Related Papers](#related-papers) | Related papers for SQuAD 2.0 |


## BERT Track

Here are the submissions that uses [BERT](https://github.com/google-research/bert), which is known to have substantial improvements than previous non-BERT models. To have a better comparison, you can regard the `BERT by Google AI Language` as the baseline scores (using BERT-large).

| System | Date | Institute | BERT | Dev-EM | Dev-F1 | Test-EM | Test-F1 | Paper | Note |
| :------- | :-----: |  :-----: |  :-----: |  :-----: |  :-----: |  :-----: |  :-----: |:-----: |:-----: |
| Lunet+Verifier+BERT | Dec 15, 2018 | Layer 6 AI NLP Team | Large | 81.504 | 84.497 | 82.994 | 86.035 | - | [note#1](#-Note-on-BERT-Track) |
| PAML + BERT | Dec 16, 2018 | PINGAN GammaLab | Large | 81.959 | 84.723 | 82.577 | 85.603 | - | - |
| BERT finetune baseline | Dec 12, 2018 | Anonymous | - | - | - | 82.125 | 84.820 | - | - |
| AoA + DA + BERT | Nov 16, 2018 | Joint Laboratory of HIT & iFLYTEK Research  | Large |  - | - | 81.178 | 84.251 | - | - |
| Candi-Net+BERT | Dec 19, 2018 | 42Maru NLP Team | Large | - | - | 80.659 | 83.562 | - | - |
| PwP + BERT | Dec 03, 2018 | AITRICS | Large | 79.339 | 82.347 | 80.117 | 83.189 | - | - |
| BERT | Nov 08, 2018 | Google AI Language  | Large | 78.741 | 81.775 | 80.005 | 83.061 | [link](https://arxiv.org/abs/1810.04805) | [code](https://github.com/google-research/bert) | 
| NEXYS_BASE | Dec 06, 2018 | NEXYS | Large | 78.194 | 81.392 | 79.779 | 82.912 | - | - |
| L6Net + BERT | Nov 09, 2018 | Layer 6 AI  | ? | 78.345 | 81.321 | 79.181 | 82.259 | - | - |
| BERT+AC | Dec 14, 2018 | Hithink RoyalFlush  | ? | - | - | 78.052 | 81.174 | - | - |
| SLQA + BERT | Nov 06, 2018 | Alibaba DAMO NLP | ? | - | - | 77.003 | 80.209 | - | - |
| *BERT_base_aug* | Nov 8, 2018 | GammaLab | Base | 75.911 | 79.027 | 76.720 | 79.610 | - | - |
| F-Net | Nov 05, 2018 | Kangwon National Univ. | ? | - | - | 74.791 | 77.988 | - | - |
| BERT+Answer Verifier | Nov 14, 2018 | Pingan Tech Olatop Lab | ? | 72.214 | 76.109 | 71.666 | 75.457 | - | pipeline |
| BASE | Nov 12, 2018 | Hithink RoyalFlush | Base | 71.868 | 75.293 | 71.496 | 74.815 | - | - |

### Note on BERT Track
1. Actually, I find this submission was not using ONE model for prediction, though they annotate their submission as 'single model'. 


## Non-BERT Track

Here are the submissions that **DO NOT** use [BERT](https://github.com/google-research/bert). But most of these models utilize [ELMo](https://allennlp.org/elmo) for enhancing the text representations. Though BERT-based models are substantially outperform these `old-day` models, it is still valuable to adopt some of these (published) techniques for future works.

| System | Date | Institute | Dev-EM | Dev-F1 | Test-EM | Test-F1 | Paper | Note |
| :------- | :-----: | :-----: |  :-----: |  :-----: |  :-----: | :-----: |  :-----: |:-----: |
| nlnet | Sep 13, 2018 | Microsoft Research Asia | - | - | 74.272 | 77.052 | - | - | 
| *YARCS* | Oct 12, 2018 | IBM Research AI | 72.273 | 75.200 | 72.670 | 75.507 | - | - |
| SLQA+ | Aug 28, 2018 | Alibaba DAMO NLP | - | - | 71.462 | 74.434 | [old-link](http://www.aclweb.org/anthology/P18-1158) | - |
| RMR + Answer Verifier | Aug 15, 2018 | NUDT | - | - | 71.767 | 74.295 | [link](https://arxiv.org/abs/1808.05759) | pipeline |
| MLAF | Sep 26, 2018 | Chonbuk National Univ. | 69.384 | 72.878 | 69.476 | 72.857 | - | - |
| Unet | Sep 14, 2018 | Fudan Univ. & Liulishuo Lab | 70.361 | 73.975 | 69.262 | 72.642 | [link](https://arxiv.org/abs/1810.06638) | - | 
| *FusionNet++* | Aug 15, 2018 | Microsoft Bussiness AI | - | - | 70.300 | 72.484 | [old-link](https://arxiv.org/abs/1711.07341) | - |
| Doc QA + NeurQuRI | Dec 20, 2018 | 2SAH | - | - | 68.766 | 71.662 | - | - |
| BiDAF++ w/ pair2vec | Sep 13, 2018 | UW and FAIR | - | - | 68.021 | 71.583 | - | - |
| *SAN* | Aug 21, 2018 | Microsoft Bussiness AI | 69.54 | 72.66 | 68.653 | 71.439 | [link](https://arxiv.org/abs/1809.09194) | [code](https://github.com/kevinduh/san_mrc) |
| VS^3-NET | Jul 13, 2018 | Kangwon National Univ. | - | - | 67.897 | 70.884 | - | - |
| GFN-NET | Jun 24, 2018 | Kangwon National Univ. | -| - | 68.213 | 70.878 | - | - |
| KakaoNet2 | Jun 25, 2018 | Kakao NLP Team | -| - | 65.719 | 69.381 | - | - |
| abcNet | Jul 11, 2018 | Fudan Univ. & Liulishuo Lab | - | - | 65.256 | 69.206 | - | - |
| BiDAF++ | Sep 13, 2018 | UW and FAIR | - | - | 65.651 | 68.866 | - | - |
| BSAE AddText | Jun 27, 2018 | reciTAL.ai | - | - | 63.338 | 67.422 | - | - |
| eeAttNet | Aug 14, 2018 | BBD NLP Team | - |- | 63.327 | 66.633 | - | - |
| Tree-LSTM + BiDAF + ELMo | Nov 27, 2018 | CMU | 59.471 | 64.213 | 57.707 | 62.341 | - | - |

### Note
1. I did not list the ensemble models here. However, if only ensemble models are available, I will list and mark it with model names in italics.
2. Anonymous submissions are ignored.
3. In `Paper` section, `link` means the submitted model is exactly what the paper illustrates. `old-link` means there is somewhat mismatch between the paper and the submitted models.
4. You will find additional scores of the development set, which is obtained from `PUBLIC` visible worksheets in CodaLab.
5. The tables are sorted by the `Test-F1` score.


## Ensemble Track

Here are the ensemble models that appeared on the leaderboard. The number of the models in ensemble is guessed by the content of these submissions (and of course it is publicly visible).

| System | Date | Institute | BERT | Model# | Dev-EM | Dev-F1 | Test-EM | Test-F1 | Note |
| :------- | :-----: |  :-----: |  :-----: |  :-----: |  :-----: |  :-----: |  :-----: |:-----: |:-----: |
| Lunet+Verifier+BERT | Dec 16, 2018 | Layer 6 AI NLP Team | Large | 8 | 83.104 | 85.403 | 83.469 | 86.043 | - |
| BERT finetune baseline | Dec 13, 2018 | Anonymous | - | - | - | - | 83.536 | 86.096 | - |
| PAML + BERT | Nov 25, 2018 | PINGAN GammaLab | Large | 10 | 82.270 | 84.723 | 83.434 | 85.991 | - |
| AoA + DA + BERT | Nov 16, 2018 | Joint Laboratory of HIT & iFLYTEK Research  | Large | 6 | - | - | 82.374 | 85.310 | - |
| Candi-Net + BERT | Dec 10, 2018 | 42Maru NLP Team | - | - | - | - | 82.126 | 84.624 | - |
| YARCS | Oct 12, 2018 | IBM Research AI | - | 20 | 72.273 | 75.200 | 72.670 | 75.507 | - |
| PAML | Nov 16, 2018 | GammaLab | - | - | 71.692 | 74.354 | 71.248 | 74.015 | - |
| Unet | Sep 17, 2018 | Fudan Univ. & Liulishuo Lab | - | 11 | 70.361 | 73.975 | 69.262 | 72.642 | - | 
| FusionNet++ | Aug 15, 2018 | Microsoft Bussiness AI | - | 2 | 72.054 | 74.239 | 70.300 | 72.484 | - |
| SAN | Aug 21, 2018 | UW and FAIR | - | - | 69.54 | 72.66 | 68.653 | 71.439 | - |


## BERT-TF and BERT-PT

Make a quick comparison of the [TensorFlow (official)](https://github.com/google-research/bert) and [PyTorch versions](https://github.com/huggingface/pytorch-pretrained-BERT) of BERT.

| - | TensorFlow | PyTorch |
| :------- | :-----: | :-----: |
| Implementation | Official | Third-party | 
| GitHub Repository | [link](https://github.com/google-research/bert) | [link](https://github.com/huggingface/pytorch-pretrained-BERT) | 
| TPU Support | Yes | No (currently)<sup>1</sup> |
| Deterministic **Training** Results | No<sup>2</sup> | Yes |
| Pre-training Script | Yes | No |
| Classifier Script | Yes | Yes |
| SQuAD 1.1 Script | Yes | Yes |
| SQuAD 2.0 Script | Yes | No<sup>3</sup> |
| SWAG Script | No | Yes |
| Flexible Evaluation | No<sup>4</sup> | Yes |
| Speed Up | - | apex<sup>5</sup> |


### Notes and Tips
1. PyTorch claims that they will support TPU in 1.0 version, but there is no further news on this.
2. It is known to all that TensorFlow suffers from reproducibility problems (in training process). That is, whether you use fixed random seed or not, you will get different results under GPU/TPU. (Yes, in CPU setting, it will be reproducible, but I don't think there is much people who uses CPU for training large-scale nerual network models.)

While PyTorch could easily get reproducible training results with the following functions (both CPU and GPU).
```
torch.backends.cudnn.deterministic = True
ramdom.seed(12345)
numpy.random.seed(12345)
torch.manual_seed(12345)
torch.cuda.manual_seed_all(12345)
```
When running the official TensorFlow implementation on SQuAD 2.0 task (i.e. `run_squad.py` script), the best score and worst score will have near **1.0 gap** in EM/F1 with the same codes and settings.
**So, it is recommended that if you use TensorFlow codes, you should run your model several times to ensure the results are reliable.**

3. The owner of the PyTorch-BERT said that they have no plans on implementing this feature, see [link](https://github.com/huggingface/pytorch-pretrained-BERT/issues/24).

4. In original `run_squad.py`, the evaluations on the `dev-v2.0.json` are only performed when the training was completely done, which is quite annoying because good results may appear in the middle checkpoints. A simple way to fix is to save all checkpoints and evaluate them at the ending of training.

5. PyTorch-BERT with [apex](https://github.com/NVIDIA/apex) could give substantial speedup, check the latest code of [PyTorch-BERT](https://github.com/huggingface/pytorch-pretrained-BERT), also check [link](https://github.com/huggingface/pytorch-pretrained-BERT/pull/116)


## Related Papers
You can download the related papers with the following links. I only list the papers that are specificly designed for SQuAD 2.0 task or reporting the results on SQuAD 2.0. 

> 1. (Rajpurkar and Jia et al., 2018) Know What You Don’t Know: Unanswerable Questions for SQuAD
<br/>http://aclweb.org/anthology/P18-2124

> 2. (Hu et al., 2018) Read + Verify: Machine Reading Comprehension with Unanswerable Questions
<br/>https://arxiv.org/abs/1808.05759

> 3. (Liu et al., 2018) Stochastic Answer Networks for SQuAD 2.0
<br/>https://arxiv.org/abs/1809.09194

> 4. (Sun et al., 2018) U-Net: Machine Reading Comprehension with Unanswerable Questions
<br/>https://arxiv.org/abs/1810.06638

> 5. (Devlin et al., 2018) BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding
<br/>https://arxiv.org/abs/1810.04805


## Statement
**If you find this repository helpful, please press the star button. Moreover, if you would like to use or repost the content in this repository, please indicate the original author and source link.**

For official leaderboard, please refer to: [http://stanford-qa.com](http://stanford-qa.com)


## Disclaimer
Any subjective comments in this repository only represents the idea of the owner (ymcui), and do not represent the claims of any organizations.


## Contact
For any problems, or if you found that I missed something, please leave a message in the `Issues` tab.

