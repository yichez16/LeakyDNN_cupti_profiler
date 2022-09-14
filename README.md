# Overview
This repository contains the source code to reproduce the experiments of the paper:
- [_Leaky DNN: Stealing Deep-learning Model Secret with GPU Context-switching Side-channel_][paper] (__DSN 2020__)

## Tested Setup
Our study is carried out on a workstation equipped with Nvidia GeForce GTX 1080 TI. 
The graphics driver version is 384.11. 
The CUDA version is V9.0.176 and the cuDNN version is 7.4.2. 
The workstation has installed Ubuntu 16.04 and we use Tensorflow 1.12.0.

## Extract GPU performance counters
To run it, you just need to type sh run_spykernel.sh.
To add more performance counters, you just need to add the names of metrics in CUPTI_Conv_Metrics.cu or event in CUPTI_Conv_Event.cu. 
The GPU performance counters will be stored into conv_metrics.csv and conv_event.csv.

## Citation

If you make any use of this code for academic purposes, please cite the paper:

```tex
@inproceedings{wei2020leaky,
  title={Leaky dnn: Stealing deep-learning model secret with gpu context-switching side-channel},
  author={Wei, Junyi and Zhang, Yicheng and Zhou, Zhe and Li, Zhou and Al Faruque, Mohammad Abdullah},
  booktitle={2020 50th Annual IEEE/IFIP International Conference on Dependable Systems and Networks (DSN)},
  pages={125--137},
  year={2020},
  organization={IEEE}
}
```

[paper]: https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9153424
[lines]: https://github.com/yichez16/LeakyDNN_cupti_profiler/blob/master/examples/CUPTI_Conv.cu#L149-L207
