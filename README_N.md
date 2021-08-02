> **Step for Data preparations**
### this is my issue
1) data is being storeed.
2) skdshksshadsjfk and  wdiss **test/shop/jeera/** kdskdjsdssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssa skdskdjsdkjs d
$workspace
      |\_\__foodnct
      
$lang  
$ cricket  
* mfkfdkf  
-skjdjsdmsd
* Samsung  
  > [link to google](https://google.com)
* Google  
* ksdjskd  
* google link     [link to google]  

1. lskadjsdkslfkslf  
   - jaksjadskdl
   - sdjskdjsldkncmxnc 

2. ksjdjfd

### Training yolo-v3 model on custum dataset  

1. For training cfg/yolo-v3.cfg download the pre-trained weights-file (162 MB): 
    > [link to Pretrained yolo-v3 weight file ](https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v3_optimal/yolov4.conv.137 )

2. Create file yolov3-obj.cfg with the same content as in yolov3-voc.cfg (or copy yolov3-voc.cfg to yolov3-obj.cfg) and:
   - change line batch to [`batch=64`]()
   - change line subdivisions to subdivisions=16
   - change line max_batches to (classes*2000, but not less than number of training images and not less than 6000), f.e. max_batches=6000 if you train for 3 classes
   - change line steps to 80% and 90% of max_batches, f.e. steps=4800,5400
   - set network size width=416 height=416 or any value multiple of 32
   - change line classes=80 to your number of objects in each of 3 [yolo]-layers:
   - change [filters=255] to filters=(classes + 5)x3 in the 3 [convolutional] before each [yolo] layer, keep in mind that it only has to be the last [convolutional] before each of the [yolo] layers.
    >  So if classes=1 then should be filters=18. If classes=2 then write filters=21. (Do not write in the cfg-file: filters=(classes + 5)x3)

      
