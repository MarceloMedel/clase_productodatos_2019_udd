
# Laboratorio: Publicando un modelo de deep learning en Heroku


> Una revisión de todo el camino necesario para publicar nuestro primer Producto de Datos. Ejemplo disponible en https://udd-image-classifier.herokuapp.com/


## Antes de empezar

- Para poder realizar este laboratorio se necesita una cuenta en [GitHub](https://www.github.com/) y [Heroku](https://www.heroku.com/). Ambas son gratuitas y les serán muy útiles en el futuro.
- Adicionalmente se asume que en el computador o máquina virtual donde se realizará el laboratorio está instalado Python y Jupyter Notebook o Jupyter Lab.
- Se recomienda generar un ambiente con Anaconda con las librerías descritas mas abajo. [Managing environment](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html)

## Instalación de librerías necesarias

### Primero creamos el ambiente Python=3.6 con conda
```
conda create -n image_classification python=3.6
````

### Pytorch

- Seguir las [instrucciones oficiales](https://pytorch.org/get-started/locally/) seleccionando el sistema operativo correspondiente.
- Para este caso se utiliza un MacBook Pro, por tanto se debe ejecutar el siguiente comando para instalar la versión estable 
```
# MAC: CPU Only
conda install pytorch torchvision -c pytorch

# Linux/Windows: CPU Only
# conda install pytorch torchvision cpuonly -c pytorch
```

### fastai [(instrucciones)](https://docs.fast.ai/install.html)
```
pip install fastai
```

### Flask [(instrucciones)](https://flask.palletsprojects.com/en/1.1.x/installation/)
```
pip install Flask
```
### Si se desea modificar aún más la aplicación web, se recomienda usar un [ambiente virtual](https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/) (además es una muy buena práctica al momento de programar en Python)

## Construcción del Modelo de Deep Learning

- Se deben seguir las instrucciones explicadas en este [notebook](https://github.com/aastroza/clase_productodatos_2019_udd/blob/master/notebooks/ejemplo_clasificador_fastai.ipynb).

## Conexión con Heroku

- El primer paso es crear una aplicación y darle un nombre.

- En "Deployment Method" escoger "Connect to Github" y seguir las instrucciones.

- Una vez que esté listo, aparecerá un link para revisar la aplicacion en el navegador, como este: https://udd-image-classifier.herokuapp.com/

## Créditos

- La construcción del modelo está basada en las clases de [Francisco Ingham y Jeremy Howard](https://github.com/fastai/course-v3/blob/master/nbs/dl1/lesson2-download.ipynb). La aplicacion web está inspirada en el trabajo de [Shankar Jha](https://github.com/shankarj67/Water-classifier-fastai).
