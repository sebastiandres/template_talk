# HELP

## Crear el ambiente
conda create -n template

# Instalar librerías
Desde requirements:
source activate template
conda install --file requirements.txt

Uno a uno:
pip install rise
pip install pandas
(rise instala jupyter notebook & all, pandas instala numpy y matplotlib)

## Generar un pdf con las slides
Ejecutar
jupyter nbconvert --to slides template.ipynb --post serve

Abrir
http://127.0.0.1:8000/template.slides.html

Agregar "?print-pdf" al enlace
http://127.0.0.1:8000/template.slides.html?print-pdf

Guardar/Imprimir como PDF

## Borrar el ambiente
conda deactivate
conda env remove -n template

## Mostrar todos los ambientes
conda env list