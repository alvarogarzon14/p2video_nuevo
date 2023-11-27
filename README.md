## **BASE VS MEGA MODELS**
This project combines BASE and MEGA models to realise real time object detection in video.
 
### **Steps to perform the detection** 
All steps must be performed from Ubuntu
 
1. Open the terminal
2. Clone the repository
   
   $git clone https://github.com/alvarogarzon14/p2video_nuevo
4. Position ourselves inside the repository folder.
   
   $cd p2video_nuevo
6. Create a virtual environment
   
   $conda create --name MEGA -y python=3.7
   
   $source activate MEGA
9. Software installation
    
   $bash instalacion.sh
11. Move to the mega.pytorch folder

    cd mega.pytorch
   
Once we have completed the steps that will allow you to create the environment on your computer with the necessary dependencies to run the code, we will launch this code both for the BASE model and for MEGA. First we will need the models of both architectures, for BASE (https://drive.google.com/file/d/1W17f9GC60rHU47lUeOEfU--Ra-LTw3Tq/view) and for MEGA (https://drive.google.com/file/d/1ZnAdFafF1vW9Lnpw-RPF1AD_csw61lBY/view).
 
We will start with the BASE model:

7. python demo/demo.py ${METHOD} ${CONFIG_FILE} ${CHECKPOINT_FILE} [--suffix ${IMAGE_SUFFIX}] [--visualize-path ${IMAGE-FOLDER}] [--output-folder ${FOLDER}] [--output-video]

python demo/demo.py base configs/vid_R_101_C4_1x.yaml R_101.pth --suffix=".JPEG" --visualize-path=image_folder --output-folder=visualizacion_BASE --output-video

Now for the MEGA model:

8. python demo/demo.py ${METHOD} ${CONFIG_FILE} ${CHECKPOINT_FILE} [--suffix ${IMAGE_SUFFIX}] [--visualize-path ${IMAGE-FOLDER}] [--output-folder ${FOLDER}] [--output-video]

python demo/demo.py mega configs/MEGA/vid_R_101_C4_MEGA_1x.yaml R_101.pth --suffix=".JPEG" --visualize-path=image_folder --output-folder=visualizacion_MEGA --output-video
