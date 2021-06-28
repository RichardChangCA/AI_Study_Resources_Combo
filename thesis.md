新闻: 医学影像AI为什么需要小数据学习？http://med.china.com.cn/content/pid/242503/tid/1026 以先验知识为基础的小样本学习: 要实现小样本学习(few-shot learning)必须要具备一些特定条件，譬如模型学习前已经吸收了一定类别的大量资料后，再加之新类别的极少量数据，最终实现小样本模型的形成。因此，小样本学习的关键是在算法中纳入合适的先验知识。利用极端变化一致性来提高数据不足情况下医学图像分割的鲁棒性: 由于医学图像的拍摄设备和拍摄环境和方式多样，各个医院和体检中心之间的人群分布差异明显，因此很难收集和标注足量的训练数据充分涵盖不同来源的图像特征。如果训练数据和实际测试数据存在明显的的分布差异（domain shift），生成的模型往往性能不佳。

新闻: 缺乏训练样本医疗AI“喂不饱”？腾讯优图实验室想了两个办法, https://vcbeat.top/42141 ,迁移学习与对抗训练数据增广

医疗影像数据集列表: https://github.com/linhandev/dataset

Semi-Supervised Learning(book pdf version): http://www.acad.bg/ebook/ml/MITPress-%20SemiSupervised%20Learning.pdf

cat: Computational Anatomy Toolbox, http://www.neuro.uni-jena.de/cat12-html/cat.html ,MATLAB version, covers diverse morphometric methods such as voxel-based morphometry (VBM), surface-based morphometry (SBM), deformation-based morphometry (DBM), and ROI- or label-based morphometry. 

Nipype: Neuroimaging in Python Pipelines and Interfaces. Interfaces.brainsuite.brainsuite. https://nipype.readthedocs.io/en/0.12.0/interfaces/generated/nipype.interfaces.brainsuite.brainsuite.html ,.nii format for skull stripping

BrainSuite Software: skull-stripping http://brainsuite.org/processing/surfaceextraction/bse/ generate brain area mask, remove neck and other muscles

Simple Skull Stripping Method: http://campar.in.tum.de/Students/DaSimpleSkullStrippingTool automated skull stripping method robust against brain diseases alternations such as resection cavity and/or brain lesions, applied for different imaging modalities.

BET (Brain Extraction Tool) deletes non-brain tissue from an image of the whole head. http://poc.vl-e.nl/distribution/manual/fsl-3.2/bet/index.html ,

Papers with code skull stripping: https://paperswithcode.com/task/skull-stripping

DeepBrain package: https://pypi.org/project/deepbrain/ ,Extract brain tissue from T1 Brain MRI (i.e skull stripping). GitHub Link: https://github.com/iitzco/deepbrain
