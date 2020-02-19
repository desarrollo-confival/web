Proyecto Pagina Web Confival en Django

# Configuración Proyecto Django-Python para pagina web en CONFIVAL

Desarrollo de pagina web Confival en framework de Django

## Instalación
A continuacion se presentan los requerimientos para configuracion de ambiente de trabajo en Windows 10. 

## Ambiente Virtual CONDA (distribución oficial de ANACONDA)

1. Instalación distribución Anaconda

```bash
instalar anaconda descargar desde https://www.anaconda.com/
```
Realizar la instalacion en el directorio raiz C:/
Seleccionar la opcion añadir a ruta de variables de entorno durante la instalación de Anaconda, esto con el fin de manipular Python e instalacion 
de librerias a travez de linea de comandos 

2. Creación del ambiente virtual

Abrir una terminal cmd Windows y ejecutar los siguientes comandos
```bash
conda update -n base -c defaults conda ==> Actualiza la version del paquete del ambiente virtual Conda 
conda create -n webconfival python=3.7.4 ==> Creacion del ambiente virtual y la versión de Python
conda activate webconfival ==> Activacion del ambiente virtual
conda deactivate ==> Desactivar ambiente virtual
pip list 

```

3. Instalar django en linea de comandos Windows, dentro del ambiente virtual webconfival activado.

```bash
pip install django==2.2.6
python -m django --version
```

4. Crear proyecto django para pagina web
```bash
django-admin startproject web
```
Estructura del proyecto creado

```bash
web/
    manage.py
    web/
        __init__.py
        settings.py
        urls.py
        wsgi.py
```

5. Instalar librerias necesarias 
```bash
pip install mysqlclient => para conectar base de datos MySQL
pip install django-ckeditor => para edicion de campo en admin
pip install Pillow => para gestion de imagenes
```
6. Configurar web/settings.py para conexion a base de datos existente Mysql en variable DATABASES

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'confival_web',
        'USER': 'root',
        'PASSWORD': '',
        'HOST': 'localhost',
    }
}
```
Configurar lenguaje del proyecto en settings.py

```python
LANGUAGE_CODE = 'es'
```
Ejecutar servidor local 

```bash
python manage.py runserver

ctrl + c  
```
<!-- ## Creacion del aplicativo core
7. Crear aplicativo "core" dentro del directorio raiz del proyecto. Este se encarga de la gestion de vistas basicas que se van a heredar
en las secciones del home page

```bash
python manage.py startapp core
```
```bash
asesores/
    __init__.py
    admin.py
    apps.py
    migrations/
        __init__.py
    models.py
    tests.py
    views.py
``` -->




