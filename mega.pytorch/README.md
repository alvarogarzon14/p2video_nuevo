## **BASE VS MEGA MODELS**
This project combines BASE and MEGA models to realise real time object detection in video.
 
### **Pasos para realizar la deteccion** 
Todos los pasos deben ser realizados desde Ubuntu
 
1. Abrir la terminal
2. Clonar el respositorio
   $git clone https://github.com/alvarogarzon14/p2video_nuevo
4. Posicionarnos dentro de la carpeta del repositorio
   $cd p2video_nuevo
5. Crear un virtual environment 
   $conda create --name MEGA -y python=3.7
   $source activate MEGA
6. Instalacion del software
   $bash instalacion.sh
7. Movernos a la carpeta mega.pytorch
 
Una vez hemos realizado los pasos que te permitirán crearte el entorno en tu ordenador con las dependencias necesarias para ejecutar el codigo, pasamos a lanzar este codigo tanto pasa el modelo BASE como para MEGA, pero antes necesitas los modelos del BASE (https://drive.google.com/file/d/1W17f9GC60rHU47lUeOEfU--Ra-LTw3Tq/view) y MEGA (https://drive.google.com/file/d/1ZnAdFafF1vW9Lnpw-RPF1AD_csw61lBY/view). 
 
Comenzaremos con el modelo BASE:
8. $ python demo/demo.py ${METHOD} ${CONFIG_FILE} ${CHECKPOINT_FILE} [--suffix ${IMAGE_SUFFIX}] [--visualize-path ${IMAGE-FOLDER}] [--output-folder ${FOLDER}] [--output-video]
python demo/demo.py base configs/vid_R_101_C4_1x.yaml R_101.pth --suffix=".JPEG" --visualize-path=image_folder --output-folder=visualizacion --output-video

Ahora realizamos el mismo procedimiento utilizando el modelo base 
9. $ python demo/demo.py ${METHOD} ${CONFIG_FILE} ${CHECKPOINT_FILE} [--suffix ${IMAGE_SUFFIX}] [--visualize-path ${IMAGE-FOLDER}] [--output-folder ${FOLDER}] [--output-video]
python demo/demo.py mega configs/MEGA/vid_R_101_C4_MEGA_1x.yaml R_101.pth --suffix=".JPEG" --visualize-path=image_folder --output-folder=visualizacion --output-video
