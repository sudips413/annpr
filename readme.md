# Automatic Nepali Number Plate Recognition System (ANNPR)

ANNPR is a system that detects Nepali number plates from vehicles and then recognizes the number in the number plates. This project was done as a minor project in 6th Semester for Computer Engineering.  

We have used YOLOv4 for number plate detection, also YOLOv4 for character segmentation and CNN for character recognition and then finally integrated all the models with django webapp for user interaction.

YOLOV4 Link: [YOLOV4](https://github.com/AlexeyAB/darknet)

This is simply integrating the models and then testing the models trained by us for user inputs. 

## Setup in your PC 

To run this app correctly first you have to install all the requirements from requirements.txt. Also better use python 3.8.5 as I used the same version
> pip install -r requirements.txt

Then download and add these two folders Own_cfg_and_weights and cnn_weights inside pytorch_YOLOv4 folder 

Own_cfg_and_weights Link: [YOLO Weights and CFG](https://drive.google.com/drive/folders/1Q6TspUqPyHtS67Ziu_tYBIcSFCsOrTMT?usp=sharing)

cnn_weights: [CNN Weights](https://drive.google.com/drive/folders/1py_ITQW1UGr5kQUSYCiwBh-C6Mw8M3cI?usp=sharing)

Also Create a folder called media in this root directory of project and inside media create another 3 folders detected_images, images, videos  
Use this format:  
annpr(root diretory):
- annpr
- frontend 
- media(new folder you created)
    - detected_images (create these 3 folders too inside media)
    - images
    - videos
- pytorch_YOLOv4
    - cnn_weights(Create a new folder with this name and add the downloaded weights from above)
    - Own_cfg_and_weights(Create a new folder with this name and add the downloaded weights from above)



To run webapp run command 
> python manage.py runserver