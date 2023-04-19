# Mask r-cnn
Basic mask-ccn project on the LabV2 dataset

by:Alok Gupta,Vincent Qi,Luke Hu

We used the [LabPics V2 dataset](https://www.cs.toronto.edu/chemselfies/) that can be downloaded from here: [V2 download](https://zenodo.org/record/4736111/files/LabPicsChemistry.zip?download=1)

The dataset is free to use under MIT license.

We will train the net to detect all the vessels and in the images and all the MaterialsAndParts in them.

The code is split into 4 sections. 

Section (1~2) are for training for mask-rcnn on Vessels and MaterialsAndParts respectively. They are split so that training can be done within the computational power constraints we had. To run edit trainDir= to point to the path of the test folder in the dataset. Section 1 trains Vessel identification and returns (int).torch where (int) is the number of training epochs. Section 2 trains detections of MaterialsAndParts and reutrn (int)mat.torch.

Section (3~4) are for runing the program on images to select image change the path in: #imgPath="/content/drive/MyDrive/Image.jpg" to point to the image you with to run on, and change the path in: "model.load_state_dict(torch.load("/content/drive/MyDrive/10000.torch", map_location=torch.device('cpu')))" to point to the trained .torch file from Sections1/2.


