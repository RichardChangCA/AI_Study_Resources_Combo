1. Youtube CS231n Stanford University Lecture 11 Detection and Segmentation: https://www.youtube.com/watch?v=nDPWywWRIRo&list=PL3FW7Lu3i5JvHM8ljYj-zLfQRF3EO8sYv&index=11

FCN: downsampling with upsampling, each pixel has one category, pixel-wise classification, max unpooling: remember the location of max value when downsampling, prevent spacial information lose. Transpose convolution(decovolution(bad name,not inverse convolution), Upconvolution, Fractionally strided convolution, Backward strided convolution): Input gives weight for filter, stride gives ratio between movement in output and input, output contains copies of the filter weighted bt the input and summing at where at overlaps in the output, need to crop some pixeles from output if out of boundary.

Image Classification with Localization: assume one object in the image, determine only one bounding box, treat localization as a regression problem, multi-task weighted loss function(weight is another hyper-parameter), a trick to train multi-task model is training one task first with other tasks freezing and then training other tasks(the idea from transfer learning),

Human Pose Estimaion: regression problem

Object Detection: sliding window(computationally expensive), region proposals(traditional image processing method, Regions of Interest(RoI), the offset is not necessarily inside the RoI) R-CNN, Fast R-CNN: RoI in feature maps, Faster R-CNN: predict region proposals with convolution layers. YOLO(You Only Look Once) and SSD(Single Shot Detection): divide image into grid and crease some base boxes from these grids. Faster R-CNN is slower but more accurate, SSD is much faster but not as accurate, Object Detection+Captioning=Dense Captioning

Mask R-CNN: instance segmentation, joint coordinates: joint object detection, post estimation and instance segmentation(multi-tak loss)

2. Youtube Semantic Segmentation https://www.youtube.com/watch?v=_N7HRnBgoCw

FCN(Fully Convolutional Network): give inputs as any sizes. The number of categories are the number of output channels. argmax scores of all channels pixel-by-pixel. pixel-wise loss function. 

Fully Convolutional DenseNets: use the idea of DenseNet in U-Net.

Fully Conneted Layer needs same input sizes.

SegNet: A deep convolutional encoder-decoder architecture for image segmentation. pooling indices in max unpooling. 
