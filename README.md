# [Arxiv 2024] LVOS: A Benchmark for Large-scale Long-term Video Object Segmentation
# [ICCV 2023] LVOS: A Benchmark for Long-term Video Object Segmentation

[<a href="https://lingyihongfd.github.io/lvos.github.io/">Home Page</a>] [<a href="https://openaccess.thecvf.com/content/ICCV2023/html/Hong_LVOS_A_Benchmark_for_Long-term_Video_Object_Segmentation_ICCV_2023_paper.html">Open Access</a>]  [<a href="https://arxiv.org/abs/2211.10181">arXiv v1</a>] [<a href="https://arxiv.org/abs/2404.19326">arXiv v2</a>]

LVOS V1 is a benchmark for long-term video object segmentation. LVOS consists of 220 videos, 120 for training(annotations public), 50 for validation(annotations public) and 50 for testing(annotations unpublic). LVOS provides each video with high-quality and dense pixel-wise annotation.

For LVOS V2, we expand the number of videos from 220 to 720, 420 for training, 140 for validation, and 160 for testing. For training and validation sets, we have released the images and annotations, while for testing set, we just publish the images and the masks of first frame.

![LVOS overview](./picture/one_pic.png)

## Dataset V2

Download LVOS V2 dataset from Google Drive ( <a href="https://drive.google.com/file/d/1-ehpl5s0Fd14WwtT-GmWtIWa_BxZl9D6/view?usp=share_link">Train</a> | <a href="https://drive.google.com/file/d/17Hwc__6i2rpF5e2s5OPqoywNxG5bzlcO/view?usp=share_link">Eval</a> | <a href="https://drive.google.com/file/d/1Vp_y8dSUO4ktYmeBFkIQnmAxK6bl3Eyf/view?usp=share_link"> Test</a> ), or Baidu Drive ( <a href="https://pan.baidu.com/s/1zNmrDyEiAVhyw6aqrSjOmg?pwd=u43g">Train</a> | <a href="https://pan.baidu.com/s/1QaPtVihs6bL5X_qn1Z6_7Q?pwd=1hb3">Eval</a> | <a href="https://pan.baidu.com/s/1KrQ_1DazHgEBtm12PCsWtA?pwd=dxhb">Test</a> ).

After unzipping image data, please download meta jsons from <a href="https://drive.google.com/drive/folders/1EtTW57QfSkUK3Jl1A_m9D120muA7NG4L?usp=share_link"> Google Drive </a> | <a href="https://pan.baidu.com/s/1AbmNJJUrLw0TDHwEv90cBw?pwd=vi7n"> Baidu Drive</a> and put them under corresponding floder.  

For the language caption, please download the meta jsons from <a href="https://drive.google.com/drive/folders/19W_SkeVW8NMv3Npzpbr60Nx5FRRwG4Tx?usp=share_link"> Google Drive </a> | <a href="https://pan.baidu.com/s/1nzh6m2s8lzV6p-YEtHr2Zw?pwd=m2ri"> Baidu Drive</a> and put them under corresponding folder.

Organize as follows:

```
{LVOS V2 ROOT}
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
    |-- train_expression_meta.json
|-- val
    |-- ...
|-- test
    |-- ...


x_meta.json
    {
        "videos": {
            "<video_id>": {
                "objects": {
                    "<object_id>": {
                        "frame_range": {
                            "start": <start_frame>,
                            "end": <end_frame>,
                            "frame_nums": <frame_nums>
                        }
                    }
                }
            }
        }
    }

x_meta_attribute.json
    {
        "sets": [
            x
        ],
        "attributes": [
            <attribute>
        ],
        "videos": {
            "<video_id>": {
                "objects": {
                    "<object_id>": {
                        "frame_range": {
                            "start": <start_frame>,
                            "end": <end_frame>,
                            "frame_nums": <frame_nums>
                        }
                    }
                },
                "set": <set>
                "attributes": [<attribute 1>, <attribute 2>]
                "num_scribbles": <num_scribbles>
                "name": <video_id>
                "image_size": [<height>, <width>]
            }
        }
    }

# <video_id> is the name of video.
# <object_id> is the same as the pixel values of object in annotated segmentation PNG files.
# <frame_id> is the 5-digit index of frame in video, and not necessary to start from 0.
# <start_frame> is the  start frame id of target object.
# <end_frame> is the  end frame id of target object.
# <frame_nums> is the number of existing frames of target object.
# <set> is the set.
# <attribute 1> is the attribute of video.
# <num_scribbles> is the number of scribbles for interactivate vos task, which is only available for validation and test set.
# <height>, <width> is the height and width of frame.

```



## Dataset V1

Download LVOS V1 dataset from Google Drive ( <a href="https://drive.google.com/file/d/1pdA1Y7-VE4coj6yacya-kolZs6hKuQpS/view?usp=share_link">Train</a> | <a href="https://drive.google.com/file/d/1msjV2AAKROc-UsXh8lUic2gQpsLKfjQ0/view?usp=share_link">Eval</a> | <a href="https://drive.google.com/file/d/1zp8uqiby3o-2jSjZOqQx4ILh-LLqTz-0/view?usp=share_link"> Test</a> ), Baidu Drive ( <a href="https://pan.baidu.com/s/1DUB27_fJO1iNmRfTYjjLkw?pwd=nff5">Train</a> | <a href="https://pan.baidu.com/s/1XAuBUvD2GFcbavVQyzgpdg?pwd=y1kr">Eval</a> | <a href="https://pan.baidu.com/s/1ObwZPfr2brPCmJ9MV89Neg?pwd=awlh">Test</a> ), or Kaggle (<a href="https://www.kaggle.com/datasets/lingyihong/longterm-vos?select=Test">Train</a> | <a href="https://www.kaggle.com/datasets/lingyihong/longterm-vos?select=Test">Eval</a> | <a href="https://www.kaggle.com/datasets/lingyihong/longterm-vos?select=Test">Test</a> ).

After unzipping image data, please download meta jsons from <a href="https://drive.google.com/drive/folders/1fOwGggoYNm_GkZIxs68ptHLk4JNF4Ebq?usp=share_link"> Google Drive </a> | <a href="https://pan.baidu.com/s/1_nrMI1cg0X8pt6_GTsRt-w?pwd=osrv"> Baidu Drive</a> | <a href="https://www.kaggle.com/datasets/lingyihong/longterm-vos?select=Test"> Kaggle </a> and put them under corresponding folder.

For the language caption, please download the meta jsons from <a href="https://drive.google.com/drive/folders/1cgIYoIXasw3nx_saYK_M8sb59rtwRFHe?usp=sharing"> Google Drive </a> | <a href="https://pan.baidu.com/s/1nP8PGx2X6LCZQ7NHyRJkVg?pwd=8dl4"> Baidu Drive</a> | <a href="https://www.kaggle.com/datasets/lingyihong/longterm-vos?select=Test"> Kaggle </a> and put them under corresponding folder.



Organize as follows:

```
{LVOS V1 ROOT}
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
    |-- train_expression_meta.json
|-- val
    |-- ...
|-- test
    |-- ...


x_meta.json
    {
        "videos": {
            "<video_id>": {
                "objects": {
                    "<object_id>": {
                        "frame_range": {
                            "start": <start_frame>,
                            "end": <end_frame>,
                            "frame_nums": <frame_nums>
                        }
                    }
                }
            }
        }
    }

x_expression_meta.json
    {
        "videos": {
            "<video_id>": {
                "objects": {
                    "<object_id>": {
                        "frame_range": {
                            "start": <start_frame>,
                            "end": <end_frame>,
                            "frame_nums": <frame_nums>
                        }
                        "caption": <caption>
                    }
                }
            }
        }
    }

# <object_id> is the same as the pixel values of object in annotated segmentation PNG files.
# <frame_id> is the 5-digit index of frame in video, and not necessary to start from 0.
# <start_frame> is the  start frame id of target object.
# <end_frame> is the  end frame id of target object.
# <frame_nums> is the number of existing frames of target object.
# <caption> is the expression to describe the target object.
```

## Evaluation

We use DDMemory as the example model to analyze LVOS. For some reasons, DDMemory is unavailable now. (DDMemory will come soon). We take advanteage of <a href="https://github.com/yoxu515/aot-benchmark" target="_blank"> AOT-T </a> as an alternative. You can download the result from <a href="https://drive.google.com/drive/folders/1bGbyNUdbvmQBBezVv_3Fp-5LITMsY2EG?usp=share_link"> Google Drive </a>

Please our <a href="https://github.com/LingyiHongfd/lvos-evaluation">evaluation toolkits</a> to assess your model's result on validation set. See this repository for more details on the usage of toolkits.

For test set, please use the <a href="https://codalab.lisn.upsaclay.fr/competitions/8767">CodaLab</a> server for convenience of evaluating your own algorithms.

## APIs

We released the tools and test scripts in this <a href="https://github.com/LingyiHongfd/LVOS-api"> repository</a>. Click on this link for more information.

## License

- The annotations of LVOS are licensed under a <a href="https://creativecommons.org/licenses/by/4.0/"> Creative Commons Attribution 4.0 License </a>.

* The evaluation toolkits of LVOS are licensed under a <a href="https://github.com/LingyiHongfd/LVOS/blob/main/LICENSE"> BSD-3-Clause license </a>.

- The data of LVOS is released for <strong>non-commercial research purpose only</strong>.

* All videos and images are from <a href="https://votchallenge.net/vot2019/results.html">VOT-LT 2019</a> , <a href="http://vision.cs.stonybrook.edu/~lasot/">LaSOT </a>, and some other datasets, which are not property of Fudan. Fudan is not responsible for the content nor the meaning of these videos and images.

## Citation

```
InProceedings{Hong_2023_ICCV,
    author    = {Hong, Lingyi and Chen, Wenchao and Liu, Zhongying and Zhang, Wei and Guo, Pinxue and Chen, Zhaoyu and Zhang, Wenqiang},
    title     = {LVOS: A Benchmark for Long-term Video Object Segmentation},
    booktitle = {Proceedings of the IEEE/CVF International Conference on Computer Vision (ICCV)},
    month     = {October},
    year      = {2023},
    pages     = {13480-13492}
}
```
