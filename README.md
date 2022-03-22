## Comparison of YOLOv5-Lite experiment results

  ID|Model | Input_size|Flops| Params | Size（M） |Map@0.5|Map@.5:0.95
 :-----:|:-----:|:-----:|:----------:|:----:|:----:|:----:|:----:|
001| yolo-fastest| 320×320|0.25G|0.35M|1.4| 24.4| -
002| YOLOv5-Lite<sub>e</sub><sup>ours</sup>|320×320|0.73G|0.78M|1.7| 35.1|-|
003| NanoDet-m| 320×320| 0.72G|0.95M|1.8|- |20.6
004| yolo-fastest-xl| 320×320|0.72G|0.92M|3.5| 34.3| -
005| YOLOX<sub>Nano</sub>|416×416|1.08G|0.91M|7.3(fp32)| -|25.8|
006| yolov3-tiny| 416×416| 6.96G|6.06M|23.0| 33.1|16.6
007| yolov4-tiny| 416×416| 5.62G|8.86M| 33.7|40.2|21.7
008| YOLOv5-Lite<sub>s</sub><sup>ours</sup>| 416×416|1.66G |1.64M|3.4| 42.0|25.2
009| YOLOv5-Lite<sub>c</sub><sup>ours</sup>| 512×512|5.92G |4.57M|9.2| 50.9|32.5| 
010| NanoDet-EfficientLite2| 512×512| 7.12G|4.71M|18.3|- |32.6
011| YOLOv5s(6.0)| 640×640| 16.5G|7.23M|14.0| 56.0|37.2
012| YOLOv5-Lite<sub>g</sub><sup>ours</sup>| 640×640|15.6G |5.39M|10.9| 57.6|39.1| 

See the wiki: https://github.com/ppogg/YOLOv5-Lite/wiki/Test-the-map-of-models-about-coco



#### Download Link：

> - [ ] `v5lite-e.pt`:   | [Baidu Drive]()  | [Google Drive]() |<br> 
>> |──────`ncnn-fp16`:   | [Baidu Drive]()  | [Google Drive](https://drive.google.com/drive/folders/1w4mThJmqjhT1deIXMQAQ5xjWI3JNyzUl?usp=sharing) |<br> 
>> |──────`ncnn-int8`: | [Baidu Drive]() | [Google Drive](https://drive.google.com/drive/folders/1YNtNVWlRqN8Dwc_9AtRkN0LFkDeJ92gN?usp=sharing) |<br> 
>> |──────`mnn-fp32`: | [Baidu Drive]() | [Google Drive](https://drive.google.com/drive/folders/1Kha3vQF-7qc5i-GFryInStgTFisGL5vq?usp=sharing) |<br> 
>> └──────tnn-fp32`: | [Baidu Drive]() | [Google Drive](https://drive.google.com/drive/folders/1VWmI2BC9MjH7BsrOz4VlSDVnZMXaxGOE?usp=sharing) |<br> 
> - [ ] `v5lite-s.pt`:   | [Baidu Drive](https://pan.baidu.com/s/1j0n0K1kqfv1Ouwa2QSnzCQ)  | [Google Drive](https://drive.google.com/file/d/1ccLTmGB5AkKPjDOyxF3tW7JxGWemph9f/view?usp=sharing) |<br> 
>> |──────`ncnn-fp16`:   | [Baidu Drive](https://pan.baidu.com/s/1kWtwx1C0OTTxbwqJyIyXWg)  | [Google Drive](https://drive.google.com/drive/folders/1w4mThJmqjhT1deIXMQAQ5xjWI3JNyzUl?usp=sharing) |<br> 
>> |──────`ncnn-int8`: | [Baidu Drive](https://pan.baidu.com/s/1QX6-oNynrW-f3i0P0Hqe4w) | [Google Drive](https://drive.google.com/drive/folders/1YNtNVWlRqN8Dwc_9AtRkN0LFkDeJ92gN?usp=sharing) |<br> 
>> |──────`mnn-fp16`: | [Baidu Drive](https://pan.baidu.com/s/12lOtPTl4xujWm5BbFJh3zA) | [Google Drive](https://drive.google.com/drive/folders/1PpFoZ4b8mVs1GmMxgf0WUtXUWaGK_JZe?usp=sharing) |<br> 
>> |──────`mnn-int4`: | [Baidu Drive](https://pan.baidu.com/s/11fbjFi18xkq4ltAKUKDOCA) | [Google Drive](https://drive.google.com/drive/folders/1mSU8g94c77KKsHC-07p5V3tJOZYPQ-g6?usp=sharing) |<br> 
>> └──────`tengine-fp32`: | [Baidu Drive](https://pan.baidu.com/s/123r630O8Fco7X59wFU1crA) | [Google Drive](https://drive.google.com/drive/folders/1VWmI2BC9MjH7BsrOz4VlSDVnZMXaxGOE?usp=sharing) |<br>                
> - [ ] `v5lite-c.pt`: [Baidu Drive](https://pan.baidu.com/s/1obs6uRB79m8e3uASVR6P1A) | [Google Drive](https://drive.google.com/file/d/1lHYRQKjqKCRXghUjwWkUB0HQ8ccKH6qa/view?usp=sharing) |<br> 
>> └──────`openvino-fp16`: | [Baidu Drive](https://pan.baidu.com/s/18p8HAyGJdmo2hham250b4A) | [Google Drive](https://drive.google.com/drive/folders/1s4KPSC4B0shG0INmQ6kZuPLnlUKAATyv?usp=sharing) |<br> 
> - [ ] `v5lite-g.pt`: | [Baidu Drive](https://pan.baidu.com/s/14zdTiTMI_9yTBgKGbv9pQw) | [Google Drive](https://drive.google.com/file/d/1oftzqOREGqDCerf7DtD5BZp9YWELlkMe/view?usp=sharing) |<br> 

Baidu Drive Password: `pogg`


```bash
$ python train.py --data coco.yaml --cfg v5lite-e.yaml --weights v5lite-e.pt --batch-size 128
                                         v5lite-s.yaml --weights v5lite-s.pt --batch-size 128
                                         v5lite-c.yaml           v5lite-c.pt               96
                                         v5lite-g.yaml           v5lite-g.pt               64
# 一、v5系列改进
$ python train.py  --img-size 640  --data myvoc.yaml --cfg models/v5Lite-c.yaml --hyp data/hyps/hyp.scratch.yaml --weights v5lite-c.pt --batch-size 8  --device 0
                                                              v5Lite-e.yaml                                            v5lite-e.pt 
                                                              v5Lite-g.yaml                                            v5lite-g.pt
                                                              v5Lite-s.yaml                                            v5lite-s.pt


# 二、yolox及改进系列：

# yoloxs-office____(纯silu，复现版，精度与官网接近)（17.2M）
$ python train.py --noautoanchor --img-size 640  --data myvoc.yaml --cfg models/yoloxs_official.yaml --hyp data/hyps/hyp.scratch.yolox.official.yaml --weights yolox-s.pt --batch-size 8 --epochs 300 --device 0

# yoloxs____(纯silu，修改后训练速度加快，精度与官网接近)（17.2M）
$ python train.py --noautoanchor --img-size 640  --data myvoc.yaml --cfg models/yoloxs_rslu.yaml --hyp data/hyps/hyp.scratch.yolox.yaml --weights yolox-s.pt --batch-size 8 --epochs 300 --device 0

# yoloxs_____(relu+silu，权重不变，推理速度加快，由于激活函数改变，精度稍微降低)（17.2M）
$ python train.py --noautoanchor --img-size 640  --data myvoc.yaml --cfg models/yoloxs.yaml --hyp data/hyps/hyp.scratch.yolox.yaml --weights yolox-s_rslu.pt --batch-size 8 --epochs 300 --device 0


# 【改进1】：前面v5的改进换上了yoloxs（头部通道为128）的head，anchor_free锚框机制

# yoloxs_Lite-c：（12.1M）
$ python train.py --noautoanchor --img-size 640  --data myvoc.yaml --cfg models/yoloxs_Lite_c.yaml --hyp data/hyps/hyp.scratch.yolox.yaml --weights v5lite-c.pt --batch-size 8 --epochs 300 --device 0

# yoloxs_Lite-e：（5.04M）
$ python train.py --noautoanchor --img-size 640  --data myvoc.yaml --cfg models/yoloxs_Lite_e.yaml --hyp data/hyps/hyp.scratch.yolox.yaml --weights v5lite-e.pt --batch-size 8 --epochs 300 --device 0

# yoloxs_Lite-g：（14.2M）
$ python train.py --noautoanchor --img-size 640  --data myvoc.yaml --cfg models/yoloxs_Lite_g.yaml --hyp data/hyps/hyp.scratch.yolox.yaml --weights v5lite-g.pt --batch-size 8 --epochs 300 --device 0

# yoloxs_Lite-s：（6.70M）
$ python train.py --noautoanchor --img-size 640  --data myvoc.yaml --cfg models/yoloxs_Lite_s.yaml --hyp data/hyps/hyp.scratch.yolox.yaml --weights v5lite-s.pt --batch-size 8 --epochs 300 --device 0


# 【改进2】：e和s系列换上了yolox-nano（头部通道为64）的head
# yoloxnano_Lite-e：（2.46M）
$ python train.py --noautoanchor --img-size 640  --data myvoc.yaml --cfg models/yoloxnano_Lite_e.yaml --hyp data/hyps/hyp.scratch.yolox.yaml --weights v5lite-e.pt --batch-size 8 --epochs 300 --device 0

# yoloxnano_Lite-s：（4.10M）
$ python train.py --noautoanchor --img-size 640  --data myvoc.yaml --cfg models/yoloxnano_Lite_s.yaml --hyp data/hyps/hyp.scratch.yolox.yaml --weights v5lite-s.pt --batch-size 8 --epochs 300 --device 0
```


## Reference

https://github.com/ultralytics/yolov5

https://github.com/ppogg/YOLOv5-Lite#readme

https://gitee.com/SearchSource/yolov5_yolox
