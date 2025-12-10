El enlace del GitHub donde se ha guardado el desarrollo de nuestro progreso es el siguiente:

https://github.com/apeas1/PIDDeteccionVehiculos.git

Al entrar se encontrara en la rama main con los siguientes directorios:

Entrega_Final/
Entrenamientos/
Modelos/
VEHICLE-DETECTION-3/
README.txt
dataset.yaml

Entrenamientos y Modelos albergan diferentes notebooks con los entrenamiento y modelos que se han ido realizando a lo largo del
proyecto.

VEHICLE-DETECTION-3 contiene las imágenes del dataset que hemos usado divididas en tres sets: train, val y test, mientras que dataset.yaml
es el fichero de configuración del dataset. Si quiere acceder al sitio de donde se ha descargado el dataset que hemos empleado en
este proyecto vaya al siguiente enlace:

https://universe.roboflow.com/sardar-vallabhbhai-national-institute-if-technology/vehicle-detection-wagr7

Entrega_Final es donde se encuentran la versión definitiva de notebooks y modelo final que hemos entrenado. Cuando acceda se encontrara
con lo siguiente:

Entrega_Final/
   | Imagenes/
	| coches.png
	| coches2.png
	| coches3.png
	| coches4.png
   | Modelo_Final/
	| best.pt
	| last.pt
   | Entrenamiento_Vehiculos_YOLOv8.ipynb
   | Modelo_Prediccion.ipynb
   | Obtencion_metricas.ipynb

El directorio Imagenes alberga las imágenes que se han usado para probar el modelo ya entrenado en el notebook Modelo_Prediccion.ipynb.

El directorio Modelo_Final contiene el modelo entrenado con epoch=30, batchsize=8 imgsize=1280, que correspondería a best.pt, representando la mejor versión del modelo. También está incluido last.pt, que es como se encontraba el modelo cuando el entrenamiento ha terminado.

El resto del directorio Entrega_Final contiene los notebooks Entrenamiento_Vehiculos_YOLOv8.ipynb, Modelo_Prediccion.ipynb y Obtencion_metricas.ipynb.

El primer notebook corresponde con el código que hemos escrito para poder entrenar los diversos modelos. Donde se realiza el entrenamiento con model.train() se pueden cambiar los hiperparámetros por si se quiere entrenar un modelo desde cero.

El segundo notebook corresponde con la predicción de los vehículos en una imagen a partir del modelo final que hemos entrenado. Tan solo sería necesario correr el código para ver que funciona. Si se quiere ver con otro de los modelos que se encuentran en el GitHub, modifique la ruta en model = YOLO(). Si quiere comprobar con otra imagen, añádala al GitHub y modifique la ruta en results = model().

El tercer notebook corresponde con las métricas del set de test del dataset que hemos utilizado para la elaboración del modelo. Si se quieren comprobar las métricas de otro modelo, modifique la ruta en model = YOLO().

Todos los notebooks han sido de elaboración propia y no hemos partido de algún GitHub externo. Tan solo se han hecho uso de librerias y herramientas externas como Pandas, OpenCV, Matplotlib3, Roboflow, NumPy y la propia librería que aporta la empresa ultralytics para poder usar YOLO.