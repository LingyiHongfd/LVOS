# LVOS: A Benchmark for Long-term Video Object Segmentation

[<a href="https://lingyihongfd.github.io/lvos.github.io/">Home Page</a>] [Paper]

LVOS is a benchmark for long-term video object segmentation. LVOS consists of 220 videos, 120 for training(annotations public), 50 for validation(annotations public) and 50 for testing(annotations unpublic). LVOS provides each video with high-quality and dense pixel-wise annotation.

## Dataset

Download LVOS dataset from Google Drive ( <a href="https://drive.google.com/file/d/1En4jfVoMJpT0XWhKe1QmG-m49OAYcdw0/view?usp=share_link">Train</a> | <a href="https://drive.google.com/file/d/1pvpsfA3BcBIjNNQV3j7aqsCkCDlgJXDP/view?usp=share_link">Eval</a> | <a href="https://drive.google.com/file/d/1qVlrTkhvpByAaHzPFwDmfEmM8tBRMhWd/view?usp=share_link"> Test</a> ), Baidu Drive ( <a href="https://pan.baidu.com/s/1WEOXuO8O5Gzg_y5QU5JxSw?pwd=c7bn">Train</a> | <a href="https://pan.baidu.com/s/1ncBi_uMYoqQdsb75mXWJkA?pwd=009x">Eval</a> | <a href="https://pan.baidu.com/s/1ttC9Eoc7vHVA5jyxIRrVug?pwd=3hkb">Test</a> ), or Kaggle (<a href="https://www.kaggle.com/datasets/lingyihong/longterm-vos?select=Test">Train</a> | <a href="https://www.kaggle.com/datasets/lingyihong/longterm-vos?select=Test">Eval</a> | <a href="https://www.kaggle.com/datasets/lingyihong/longterm-vos?select=Test">Test</a>).

After unzipping image data, please download meta jsons from <a href="https://drive.google.com/drive/folders/1faJvd2O1qei7eeaZogbYO3NrXOmq6Hkg?usp=share_link"> Google Drive </a> | <a href="https://pan.baidu.com/s/1Il3YVpw7-A7-gaV99ylsrA?pwd=um4p"> Baidu Drive</a> | <a href="https://www.kaggle.com/datasets/lingyihong/longterm-vos?select=Test"> Kaggle </a> 



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
    |-- train_meta.json
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
