Creacion y activacion de entrono virtual :
    py -m venv entorno <!-- cracion -->
    cd entorno/scripts  <!-- direccion -->
    .\activate   <!-- activacion -->

Tecnologias al instalar con el entorno activo:
    python.exe -m pip install --upgrade pip <!-- actializacion del pip y py -->
    pip install django <!-- framework -->
    pip install unipath  <!-- configurar estructura -->
    pip install psycopg2  <!-- ORM para PostgreSQL -->
    pip install pillow <!-- trabajo con imagenes -->


Verificacion base de datos PostgreSQL:  <!-- en  base a esto debe hacer la base de tatos en le shell de PostgreSQL-->
    DATABASES = {
        'default': {
            'ENGINE': 'django.db.backends.postgresql_psycopg2',   <!-- de ley , indica con q motor trabajara y la ORM -->
            'NAME': 'biblioteca',   <!-- nombre de la base de datos -->
            'USER': 'cris',  <!-- usuario con accesos -->
            'PASSWORD': 'cris2003',  <!-- contraseña de la BD -->
            'HOST': 'localhost',  <!-- de ley -->
            'PORT': '5432',   <!-- de ley -->
            'OPTIONS': {
                'client_encoding': 'UTF8',
            },
        }
    }

Probar si corre el proyecto despues de instalar las tecnologias :
    (cd..) * 2  <!-- ir a la altura del archivo manage.py -->
    py manage.py runserver   <!-- codigo para correr un servidor local -->

Crear un usuario admin al comprar q corre todo:
    py manage.py createsuperuser  <!-- codigo para cear un usuario administrador -->
    <!-- tener presente usuario y password -->

crear aplicaciones :
    cd applications   <!-- direccion --> 
    django-admin startapp <NombreApp>   <!-- codigo creacion app -->
    INSTALLED_APPS = [
        'django.contrib.admin',
        'django.contrib.auth',
        'django.contrib.contenttypes',
        'django.contrib.sessions',
        'django.contrib.messages',
        'django.contrib.staticfiles',
        <!-- COLOCAR LAS APPS CREADAS -->
        'applications.<NombreDeLaApp>   <!-- copia y pega en el name de app.py  -->
    ]


CODIGOS BASICOS GIT
    <!-- 
    git init
    git add  o git rm para eliminar cosas (delete o modificacioone)
    git commit -m "COMENTARIOS"
    git remote -v
    git remote add origin <URL Repositorio>
    git push -u origin main 
    -->