**Note that, this repository will be updated irregularly.**

## Statement
**If you find this repository helpful, please press the star button. Moreover, if you would like to use or repost the content in this repository, please indicate the orignal author and source link.**

For official leaderboard, please refer to: [http://stanford-qa.com]()


### BERT Track

| System | Date | Institute | BERT | Dev-EM | Dev-F1 | Test-EM | Test-F1 | Paper | Note |
| :------- | :-----: |  :-----: |  :-----: |  :-----: |  :-----: |  :-----: |  :-----: |:-----: |:-----: |
| PAML + BERT | Nov 25, 2018 | PINGAN GammaLab | Large | - | - | 81.347 | 84.560 | - |
| AoA + DA + BERT | Nov 16, 2018 | Joint Laboratory of HIT & iFLYTEK Research  | Large |  - | - | 81.178 | 84.251 | - |
| PwP + BERT | Dec 03, 2018 | AITRICS | Large | 79.339 | 82.347 | 80.117 | 83.189 | - |
| Candi-Net+BERT | Dec 05, 2018 | AITRICS | Large | - | - | 80.388 | 82.908 | - |
| BERT | Nov 08, 2018 | Google AI Language  | Large | 78.741 | 81.775 | 80.005 | 83.061 | [link](https://arxiv.org/abs/1810.04805) | [code](https://github.com/google-research/bert) | 
| L6Net + BERT | Nov 09, 2018 | Layer 6 AI  | ? | 78.345 | 81.321 | 79.181 | 82.259 | - |
| SLQA + BERT | Nov 06, 2018 | Alibaba DAMO NLP | ? | - | - | 77.003 | 80.209 | - |
| BERT+Answer Verifier | Nov 14, 2018 | Pingan Tech Olatop Lab | ? | 72.214 | 76.109 | 71.666 | 75.457 | - |
| BERT_base_aug | Nov 8, 2018 | GammaLab | base | 75.911 | 79.027 | 76.720 | 79.610 | - | ensemble |


### Non-BERT Track

| System | Date | Institute | Dev-EM | Dev-F1 | Test-EM | Test-F1 | Paper | Note |
| :------- | :-----: | :-----: |  :-----: |  :-----: |  :-----: | :-----: |  :-----: |:-----: |
| F-Net | Nov 05, 2018 | Kangwon National Univ. | - | - | 74.791 | 77.988 | - | - | 
| nlnet | Sep 13, 2018 | Microsoft Research Asia | - | - | 74.272 | 77.052 | - | - | 
| BASE | Nov 12, 2018 | Hithink RoyalFlush | - | - | 71.496 | 74.815 | - | - |
| SLQA+ | Aug 28, 2018 | Alibaba DAMO NLP | - | - | 71.462 | 74.434 | [old-link](http://www.aclweb.org/anthology/P18-1158) | - |
| RMR + Answer Verifier | Aug 15, 2018 | NUDT | - | - | 71.767 | 74.295 | [link](https://arxiv.org/abs/1808.05759) | - |
| Unet | Sep 14, 2018 | Fudan Univ. & Liulishuo Lab | - | - | 69.262 | 72.642 | [link](https://arxiv.org/abs/1810.06638) | - | 
| FusionNet++ | Aug 15, 2018 | NUDT | - | - | 71.767 | 74.295 | [old-link](https://arxiv.org/abs/1711.07341) | ensemble |
| MLAF | Sep 26, 2018 | Chonbuk National Univ. | - | - | 69.476 | 72.857 | - | - |
| BiDAF++ w/ pair2vec | Sep 13, 2018 | UW and FAIR | - | - | 68.021 | 71.583 | - | - |
| SAN | Aug 21, 2018 | UW and FAIR | - | - | 68.021 | 71.583 | [link](https://arxiv.org/abs/1809.09194) | [code](https://github.com/kevinduh/san_mrc) |
| VS^3-NET | Jul 13, 2018 | Kangwon National Univ. | - | - | 67.897 | 70.884 | - | - |
| GFN-NET | Jun 24, 2018 | Kangwon National Univ. | -| - | 68.213 | 70.878 | - | - |
| KakaoNet2 | Jun 25, 2018 | Kakao NLP Team | -| - | 65.719 | 69.381 | - | - |
| abcNet | Jul 11, 2018 | Fudan Univ. & Liulishuo Lab | - | - | 65.256 | 69.206 | - | - |
| BiDAF++ | Sep 13, 2018 | UW and FAIR | - | - | 65.651 | 68.866 | - | - |
| BSAE AddText | Jun 27, 2018 | reciTAL.ai | - | - | 63.338 | 67.422 | - | - |
| eeAttNet | Aug 14, 2018 | BBD NLP Team | - |- | 63.327 | 66.633 | - | - |
| Tree-LSTM + BiDAF + ELMo | Nov 27, 2018 | CMU | - | - | 57.707 | 62.341 | - | - |


### Note
1. I did not list the ensemble models here. However, if only ensemble models are available, I will list and mark it as ensemble.
2. Anonymous submissions are ignored.
3. In `Paper` section, `link` means the submitted model is exactly what the paper illustrates. `old-link` means there is somewhat mismatch with the paper and the submitted models.
4. You will find additional score of the development set, which is obtained from `PUBLIC` visible worksheets in CodaLab.


## Contact
For any problems, please leave a message in the `Github Issues`.


## Disclaimer
Any subjective comments in this repository only represents the idea of the owner (ymcui), and does not represent the claims of any organizations.
