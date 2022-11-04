# LVOS: A Benchmark for Long-term Video Object Segmentation

[<a href="https://lingyihongfd.github.io/lvos.github.io/">Home Page</a>] [Paper]

LVOS is a benchmark for long-term video object segmentation. LVOS consists of 220 videos, 120 for training(annotations public), 50 for validation(annotations public) and 50 for testing(annotations unpublic). LVOS provides each video with high-quality and dense pixel-wise annotation.

## Dataset

Download LVOS dataset from Google Drive ( <a href="https://drive.google.com/file/d/117TIQr9UiQpO2wkX-RH0a1r9q1eHppQc/view?usp=sharing">Train</a> | <a href="https://drive.google.com/file/d/1kRh9zgtdibrkBr2cQYwfScJoZOFhmlat/view?usp=sharing">Eval</a> | <a href="https://drive.google.com/file/d/1YOWdjHw-St8TDx8XM1CHYh8yUYxM__YH/view?usp=sharing"> Test</a> ), Baidu Drive ( <a href="https://pan.baidu.com/s/1CmRcqPsjp6Xq8Q33gF40HA?pwd=4sfc">Train</a> | <a href="https://pan.baidu.com/s/1y6cW8DbF98xa8fAreW__Gw?pwd=8u86">Eval</a> | <a href="https://pan.baidu.com/s/1SBgiGSF-xnWPz26lvI4bAw?pwd=k542">Test</a> ), or Kaggle (<a href="https://www.kaggle.com/datasets/lingyihong/longterm-vos?select=Test">Train</a> | <a href="https://www.kaggle.com/datasets/lingyihong/longterm-vos?select=Test">Eval</a> | <a href="https://www.kaggle.com/datasets/lingyihong/longterm-vos?select=Test">Test</a>).

Organize as follows:

```
{LVOS ROOT}
|-- train
    |-- JPEGImages
        |-- video1
            |-- 00000001.jpg
            |-- ...
    |-- Annotations
        |-- video1
            |-- 00000001.jpg
            |-- ...
    |-- meta.json
|-- val
    |-- ...
|-- test
    |-- ...
```

## Evaluation

We use DDMemory as the example model to analyze LVOS. For some reasons, DDMemory is unavailable now. (DDMemory will come soon). We take advanteage of <a href="https://github.com/yoxu515/aot-benchmark" target="_blank"> AOT-T </a> as an alternative.

Please <a href="https://github.com/LingyiHongfd/lvos-evaluation">our evaluation toolkits</a> to assess your model's result on validation set. See this repository for more details on the usage of toolkits.

For test set, please use the <a href="https://github.com/LingyiHongfd/LVOS">CodaLab</a> server for convenience of evaluating your own algorithms.

## License

- The annotations of LVOS are licensed under a <a href="https://creativecommons.org/licenses/by/4.0/"> Creative Commons Attribution 4.0 License </a>.

* The evaluation toolkits of LVOS are licensed under a <a href="https://github.com/LingyiHongfd/LVOS/blob/main/LICENSE"> BSD-3-Clause license </a>.

- The data of LVOS is released for <strong>non-commercial research purpose only</strong>.

* All videos and images are from <a href="https://votchallenge.net/vot2019/results.html">VOT-LT 2019</a> and <a href="http://vision.cs.stonybrook.edu/~lasot/">LaSOT </a>, which are not property of Fudan. Fudan is not responsible for the content nor the meaning of these videos and images.

## Citation
