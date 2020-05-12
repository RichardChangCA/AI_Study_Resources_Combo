* Codes, Image Segmentation Practice: https://github.com/RichardChangCA/Image_Segmentation_Practice

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

3. Medium, Metrics to Evaluate your Semantic Segmentation Model: https://towardsdatascience.com/metrics-to-evaluate-your-semantic-segmentation-model-6bcb99639aa2 , Pixel Accuracy, Intersection-Over-Union (IoU), Dice Coefficient

4. Medium, DilatedNet — Dilated Convolution (Semantic Segmentation, year 2016)  https://towardsdatascience.com/review-dilated-convolution-semantic-segmentation-9d5a5bd768f5 ,the idea of Dilated convolution is proposed in semantic segmentation, atrous convolution.

5. Medium, DeconvNet: https://towardsdatascience.com/review-deconvnet-unpooling-layer-semantic-segmentation-55cf8a6e380e ,upsampling, deconvolution, two-stage training(first stage for region proposal-object detection, second stage for instance segmentation), segmentation(sparse pixel-wise classification, semantic: crop all person as a kind of person, instance: crop different person as A,B,C... ). deconvolution is not the reverse process of convolution, and it is the fractional stride convolution.

6. Medium, FCN in semantic segmentation: https://towardsdatascience.com/review-fcn-semantic-segmentation-eb8c9b50d2d1 ,deeper layers can extract deeper features but lose the spatial location information of objects in the image, shallow layers have spatial location information, fuse shallow and deep features can combine the spatial location information and object information together to do a better semantic segmentation.

7. Medium, DeepLabV1 and DeepLabV2(semantic segmentation): https://towardsdatascience.com/review-deeplabv1-deeplabv2-atrous-convolution-semantic-segmentation-b51c5fbde92d , image->Atrous convolution(hole convolution, dilated convolution)->Atous Spatial Pyramid Pooling(ASPP)->bilinear interpolation to do upsampling-> fully connected conditional random field(CRF), which is a post-processing process, making two frameworks not end-to-end semantic segmentation. multi-scale input is a trick to improve model accuracy a little.

8. Medium, SPPNet: https://medium.com/coinmonks/review-sppnet-1st-runner-up-object-detection-2nd-runner-up-image-classification-in-ilsvrc-906da3753679 , spatial pyramid pooling(SPP): multiple pooling layers with different scales. With SPP, variable sizes are accepted as input, different sizes should be fed into network to increase the robustness of the network during traning.

9. Medium, PSPNet (Pyramid Scene Parsing Network): https://towardsdatascience.com/review-pspnet-winner-in-ilsvrc-2016-semantic-segmentation-scene-parsing-e089e5df177d , PSP can extract more global information than FCN. Weighted Auxiliary loss is used in training PSPNet.

10. Medium, DeepLabV3 https://towardsdatascience.com/review-deeplabv3-atrous-convolution-semantic-segmentation-6d818bfd1d74 ,DeepLabV3 do not use CRF. model without atrous conv will lose the information of location when goes deeper. Spatial information is also important for segmentation tasks. Multi-grid atrous rate during convolution. Just some small changes based on DeepLabV2. DeepLabV3+ performs better than DeepLabV3.

11. Medium, ParseNet(2016): https://medium.com/datadriveninvestor/review-parsenet-looking-wider-to-see-better-semantic-segmentation-aa6b6a380990 ,get more global context(globle pooling), normalization using L2 norm for each channel(earlier layers usually have larger values than the later layers, which is probably also the reason why batch normalization works well after that), a learnable scaling factor γ for each channel is also introduced after normalization. ParseNet is used in DeepLabV3 and DeepLabV3+.

12. Medium, The Evolution of Deeplab for Semantic Segmentation: https://towardsdatascience.com/the-evolution-of-deeplab-for-semantic-segmentation-95082b025571 ,DeepLab V1, V2, V3, V3+. three main methods in semantic segmentation: fully convolutional network(FCN), U-Net and DeepLab(last two are commonly used recently). one advantage of FCN(without fully connected layers) is inputs can be any sizes, (the architecure with fully connected layers needs the input size fixed because the number of parameters in fully connected layers is fixed), atrous convolution enlarges the field of view of filters without increasing the number of parameters or the amount of computation. Atrous(hole in English, trous in French) convolution can replace downsampling with upsampling to avoid spatial information loss, evolving from FCN to DeepLabV1.

- Traditional CNN: CNN+fully connected layer. 

- FCN(based on traditional CNN): replace fully connected layers with convolutional layers and pixel-wise loss function. 

- DeepLabV1(based on FCN): replace later convolution layers with atrous convolution + bi-linear interpolation + CRF. 

- DeepLabV2(based on DeepLabV1): add atrous spatial pyramid pooling(ASPP): apply multiple atrous covolution with different sampling rates and fuse together, tackling the problem of scaling objects. 

- DeepLabV3(based on DeepLabV2): encoder-decoder with atrous separable convolution(computational efficiency) to capture shaper object boundaries.  

- DeepLabV3+(based on DeepLabV3): changed encoder from ResNet-101 to Aligned Xception. The decoder combines shallow and deep  feature maps of the encoder together.
