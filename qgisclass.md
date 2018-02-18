
---
title: Principios de Estadística Aplicada con R
subtitle: Introducción a R
Project: 
author:
- name: Gabriel Carrasco Escobar
  affiliation: Universidad Peruana Cayetano Heredia
- name: Jorge Ruiz Cabrejos
  affiliation: Universidad Peruana Cayetano Heredia
Comment:
web: 
date: 08 de febrero del 2018
output: 
  html_document:
    toc: true
    toc_float: true
---

# Descripción de Procedimientos

## Instalación del programa

<ol> 
    <li>Ingresar a la página web de QGIS: http://www.qgis.org/ y descargar la última versión de QGIS. Para la presente práctica usaremos la versión 2.12 Lyon. </li>
</ol>
<ul> 
    <li>Opción “Descargar Ahora”</li>
    <li>Pestaña “Descargas de instalación”</li>
    <li>Sección “Último lanzamiento (eg. para Nuevos Usuarios):”</li>
    <li>Escoger de acuerdo a la configuración de su computadora la versión de 32 o 64 bit</li>
    <li>Ejecutar el programa descargado</li>

</ul>


## Descripción General del programa
<ol start="2">
    <li>QGIS cuenta con 4 secciones importantes que hay que identificar antes de empezar el trabajo:
    </li>
</ol>
<ul> 
    <li>Menú y controles</li>
    <li>Ventana de visualización de datos</li>
    <li>Tabla y contenidos</li>
    <li>Importación de datos</li>
</ul>

<div align="left"><img src="C:\Users\CORE_DM\Desktop\qgis\images\imagen2.png" width=500 ></div>




## Datos Vectoriales: Importación
<ol start="3">
    <li>En la sección Importación de datos, hacer click en Agregar capa vectorial <div align="left"><img src="C:\Users\CORE_DM\Desktop\qgis\images\imagen1.png" width=40 height=40></div></li>
    <li>Agregar al área de trabajo todos los archivos .shp de la carpeta “CAPAS”.</li>
    <li>Hacer click izquierdo sobre la capa importada y seleccionar Zoom to layer para visualizarla en la ventana de visualización de datos.</li>
    <li>Seleccionar y arrastar las capas dentro de la Tabla de contenidos para ordenarlas.</li>
    <li>Para guardar el proyecto, hacer click en Guardar dentro de la sección de Menú y controles, y seleccionar la dirección donde se guardará el proyecto.</li>
</ol>


## Datos Vectoriales: Manejo de atributos
<ol start="8">
    <li>Seleccionar la capa ríos dentro de la Tabla de contenidos</li>
    <li>Hacer click en Abrir tabla de atributos <div align="left"><img src="C:\Users\CORE_DM\Desktop\qgis\images\imagen3.png" width=40 height=40></div> en el Menú y controles.</li>
    <li>Observar los datos que contiene la capa.</li>
    <li>Dentro de Menú y controles, hacer click en Seleccionar atributo por área <div align="left"><img src="C:\Users\CORE_DM\Desktop\qgis\images\imagen4.png" width=40 height=40></div></li>
    <li>Seleccionar algún elemento de la capa ríos. Se sombreará de amarillo el elemento si la selección ha sido correcta.</li>
    <li>Hacer click en Abrir tabla de atributos.</li>
    <li>Hacer click en Mover la selección Arriba <div align="left"><img src="C:\Users\CORE_DM\Desktop\qgis\images\imagen5.png" width=40 height=40></div>, dentro de Tabla de atributos.</li>
</ol>


## Datos Vectoriales: Simbología de capas
<ol start="15">
    <li>Seleccionar la capa ciudades dentro de la Tabla de contenidos</li>
    <li>Hacer click izquierdo y seleccionar propiedades.</li>
    <li>Ir a la sección Estilo.</li>
    <li>Seleccionar la opción Single Symbol.</li>
    <li>Cambiar el color, grosor y apariencia de la línea.</li>
    <li>Ver en la ventana de visualización de datos los cambios realizados.</li>
    <li>Repetir pasos del 17 al 19</li>
    <li>Seleccionar la opción Categorized.</li>
    <li>En Column seleccionar el atributo ADM1NAME.</li>
    <li>Hacer click en Classify.</li>
    <li>Ver en la ventana de visualización de datos los cambios realizados.</li>
    <li>Repetir pasos del 17 al 19</li>
    <li>Seleccionar la opción Graduated.</li>
    <li>En Column seleccionar el atributo ELEVATION.</li>
    <li>Hacer click en Classify.</li>
    <li>Ver en la ventana de visualización de datos los cambios realizados.</li>
    
</ol>


## Datos vectoriales: Geoprocesos básicos
<ol start="31">
    <li>Ir a la barra de herramientas – vectorial – herramientas de geoproceso -> Cortar.</li>
    <li>Establecer capa vectorial de entrada -> ciudades.</li>
    <li>Establecer capa de corte -> zona_estudio.</li>
    <li>Establecer ruta de archivo shape de salida. Aceptar. Cerrar. (poner nombre de archivo: ‘ciudades_clip.shp’).</li>
    <li>En el Panel de capas, dar click derecho a la capa ciudades – Estilos – Copiar estilo.</li>
    <li>En el Panel de capas, dar click derecho a la capa ciudades_clip – Estilos – Pegar estilo.</li>
    <li>Abrir tabla de atributos de la capa ciudades_clip, Hacer click en el símbolo <div align="left"><img src="C:\Users\CORE_DM\Desktop\qgis\images\imagen6.png" width=40 height=40></div> (cntrl + E).</li>
    <li>Hacer click en el símbolo <div align="left"><img src="C:\Users\CORE_DM\Desktop\qgis\images\imagen7.png" width=40 height=40></div> Anadir campo (cntrl + W), establecer nombre ‘size_cor’, tipo ‘Numero decimal’, longitud 10, precisión 9 – Aceptar.</li>
    <li>En el símbolo <div align="left"><img src="C:\Users\CORE_DM\Desktop\qgis\images\imagen8.png" width=70 height=40></div> seleccionar size_cor, en campo de escritura ubicado a la derecha, escribir ‘SIZE/25, hacer click en Actualizar todo, ubicado a la derecha del campo de escritura.</li>
    <li>Hacer click en <div align="left"><img src="C:\Users\CORE_DM\Desktop\qgis\images\imagen9.png" width=40 height=40></div> (cntrl + G), hacer click en <div align="left"><img src="C:\Users\CORE_DM\Desktop\qgis\images\imagen10.png" width=40 height=40></div> (cntrl + E). Cerrar la ventana.</li>
    <li>Ir a la barra de herramientas – vectorial – herramientas de geoproceso -> Buffer.</li>
    <li>Establecer capa vectorial de entrada -> ciudades_clip, seleccionar campo de distancia de buffer -> size_cor, establecer archivo shape de salida (‘ciudades_buffer’).</li>
</ol>


## Instalación de Complementos (Plugins)
<ol start="43">
    <li>Ir a la barra de herramientas – Complementos.</li>
    <li>En el campo buscar escribir ‘OpenLayers’, seleccionar OpenLayers Plugin y hacer click en instalar complemento.</li>
    <li>Ir a la barra de herramientas – Web- OpenLayers Plugin –OpenStreetMap –> OpenStreetMap. (se debe tener conexión a internet)</li>
</ol>


## Datos Vectoriales: Exportación
<ol start="46">
    <li>Seleccionar la capa ciudades dentro de la Tabla de contenidos.</li>
    <li>Hacer click izquierdo y seleccionar Guardar como.</li>
    <li>Seleccionar Formato Comma Separated Value [CSV].</li>
    <li>Seleccionar Coordinate Reference System (CRS) correcto. En este caso (EPSG:4326, WGS 84).</li>
    <li>Seleccionar la dirección donde se va a guardar el archivo.</li>
    <li>Hacer click en Ok.</li>
</ol>

