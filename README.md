# lion_share

> lion复现结果共享

| GPUs*BS |    LR    |  mAP  |  NDS  | mATE | mASE | mAOE | mAVE | mAAE | DEVICE |                                  CFG                                  |                         LOG                         |       EXPLAIN       |
| :-----: | :------: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :----: | :--------------------------------------------------------------------: | :--------------------------------------------------: | :-----------------: |
|   8*2   |  0.003  | 68.00 | 72.10 |   -   |   -   |   -   |   -   |   -   |   -   |                                   -                                   |                          -                          |   原文给出的结果   |
|   8*2   |  0.003  | 67.75 | 72.17 |   -   |   -   |   -   |   -   |   -   | autodl |                                   -                                   |                          -                          |  8卡复现结果，nzw  |
|   4*2   |  0.003  | 66.50 | 70.80 |   -   |   -   |   -   |   -   |   -   | autodl |                                   -                                   |                          -                          |  4卡复现结果，nzw  |
|   2*2   |  0.003  | 65.90 | 70.40 |   -   |   -   |   -   |   -   |   -   | autodl |                                   -                                   |                          -                          |  2卡复现结果，nzw  |
|   2*1   |  0.003  | 62.95 | 68.24 | 28.54 | 25.97 | 30.13 | 28.66 | 19.10 |  4091  | [cfg](assets/lr_3e3_2x1/lion_mamba_nusc_8x_1f_1x_one_stride_128dim.yaml) | [log](assets/lr_3e3_2x1/log_train_20250218-193740.txt) |   未线性缩放，zgm   |
|   2*1   | 0.00075 | 65.98 | 70.62 | 26.98 | 24.70 | 27.65 | 25.14 | 19.24 |  3090  | [cfg](assets/lr_75e4_2x1/lion_mamba_nusc_8x_1f_1x_one_stride_128dim.yaml) | [log](assets/lr_75e4_2x1/log_train_20250307-142818.txt) |  双倍线性缩放，zgm  |
|   1*2   | 0.000375 | 66.14 | 71.07 | 26.81 | 24.54 | 25.66 | 24.35 | 18.65 |  4091  |                                   -                                   |                          -                          | 正确的线性缩放，lcf |
