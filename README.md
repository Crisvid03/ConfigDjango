Creacion y activacion de entrono virtual :
py -m venv entorno <!-- cracion -->
cd entorno/scripts  <!-- direccion -->
.\activate   <!-- activacion -->

Tecnologias al instalar con el entorno activo:
python.exe -m pip install --upgrade pip <!-- actializacion del pip y py -->
pip install django <!-- framework -->
pip install unipath  <!-- configurar estructura -->
pip install psycopg2  <!-- ORM para PostgreSQL -->


Verificacion base de datos PostgreSQL:

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql_psycopg2',   <!-- de ley indica con q motor trabajara -->
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
py manage.py runserver