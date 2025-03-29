# lion_share
> lion复现结果共享

| GPUs*BS | LR | mAP | NDS | mATE | mASE | mAOE | mAVE | mAAE | DEVICE | CFG | LOG | EXPLAIN |
| :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: |
| 2*1 | 0.003 | 62.95 | 68.24 | 28.54 | 25.97 | 30.13 | 28.66 | 19.10 | 4091 | [cfg](assets\lr_3e3_1x2\lion_mamba_nusc_8x_1f_1x_one_stride_128dim.yaml) | [log](assets\lr_3e3_1x2\log_train_20250218-193740.txt) |  |
| 2*1 | 0.00075 | 65.98 | 70.62 | 26.98 | 24.70 | 27.65 | 25.14 | 19.24 | 3090 | [cfg](assets\lr_75e4_1x2\lion_mamba_nusc_8x_1f_1x_one_stride_128dim.yaml) | [log](assets\lr_75e4_1x2\log_train_20250307-142818.txt) |  |
| 1*2 | 0.000375 | - | - | - | - | - | - | - | 4091 | - | - | running |
