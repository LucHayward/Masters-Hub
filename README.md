# Learning to Clean Heritage Point Clouds
This is a central hub for linking together the different repositories created during the course of my Masters Research.

# Abstract
Laser scanning technology enables accurate distance measurements between a scanner and the environment producing a grid of points in 3D space. 
Many laser scans can be registered together to produce a "point cloud". This is commonly used in the Cultural Heritage domain to create highly detailed 3D models. However, the raw point cloud often contains unwanted details and artefacts which require manual removal through a time-consuming process called point cloud cleaning.

Whilst previous works have shown promising results, the application of deep learning in the cultural heritage domain has not been fully explored. 
In this study, we investigate the use of deep learning models for the binary segmentation of semantically varied cultural heritage sites using a few-shot fine-tuning approach. 
By relying only on learned geometric information without additional point attributes such as colour, we demonstrate the effective application of modern deep learning approaches in this domain.
% and maintain their relative performance across our heritage datasets.

We present a method in which the user is presented with an unlabelled scan and asked to label a percentage between 2.5-50% of the scene. This labelled data is used to train the model and predict labels for the remainder of the scene.
We compare the performance of three different deep learning models (Pointnet++, KPConv, and Point Transformer) against a baseline Random Forest model. 
We consider factors such as speed, pretraining, and the amount of hand labelling required.

Our results show that minimal human labelling is needed to provide sufficient data for modern deep learning approaches and simple scenes are efficiently labelled using Random Forests.
We achieve up to 90% mean Intersection over Union on the remaining points, with as little as 5% of the scene labelled for training, in under two hours on consumer hardware.
This translates to a reduction in manual labelling effort of up to 90%.

Among the models tested, KPConv reliably produces good results with minimal need for human labelling. The remaining models are slower to train and required more human labelling, while the Random Forest is effective only on simple scans, where a machine learning model would be inefficient to train.

Our work demonstrates the potential of deep learning methods for label-efficient and accurate point cloud cleaning in the cultural heritage domain, reducing the time spent on manual cleaning.

# Repositories
With the exception of the early work, the three model repositories link to my fork of their code and include the changes made to adapt the models to my experiments. These repositories are in the general state of dissarray typical of a research project, I aim to clean them up as and when I feel motivated.
## [Early Work](https://github.com/LucHayward/Masters-PointClouds)

## [Pointnet++](https://github.com/LucHayward/Pointnet_Pointnet2_pytorch)
This repository includes:
1. The majority of our data visualisation notebooks and main experimental results including code to read these into Pandas DataFrames
2. The implementation of our Random Forest experiments
3. The implementation of our Active Learning experiments
4. Our custom data loading scripts including additional optimisations over the original methods
## [KPConv](https://github.com/LucHayward/KPConv-PyTorch)
Additional modified scripts for handling our datasets and experiments on a slurm cluster.
## [Point Transformer](https://github.com/LucHayward/point-transformer)


# Experimental Results
This repo contains our full raw experimental results as well as several views into the data which extract useful insights for our analysis.
