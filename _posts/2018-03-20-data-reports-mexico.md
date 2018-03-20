---
layout: post
title: Digital National Newspaper Library of Mexico, Hemeroteca Nacional Digital de México
tags: [dh, DiD, data reports]
author: igalina, alerma
---

# Digital National Newspaper Library of Mexico
_Report also available in [Español](#espanol)_

## Collection History
México’s National Digital Newspaper Library (HNDM, in Spanish) was created between 2004 and 2008.  Like many libraries at that time, these new digital storage methods were used both to preserve the originals as well as to provide increased access. 

The project focused on digitalizing México’s National Newspaper Library’s microfilm collection, which was created in 1960. The documents were selected according to the following criterion: the newspaper’s degree of conservation, the demand as well as their historical, patrimonial, journalistic, and documentary importance. In this way the digitization project aimed to offer new forms of access and use of the historical newspapers, including search options by word, phrase, year and date range. 

## Collection composition
Today, the HNDM has almost 8 million digitized pages from 941 newspaper titles between 1722 and 2006. Out of these, 516 titles (1722-1889) are Open Access, and 425 (1890-2006) are restricted and can only be accessed from inside the Newspaper Library’s facilities.

The microfilmed and digital archives can be found in the National Newspaper Library’s _Fondo Reservado_ (special collections) which includes: Mexican periodical publications between 1722 and 1917; foreign periodical publications from 1665 to 1920; the Garcia Valseca collection and the newspaper miscellanea and important newspapers microfilms collections (Hemeroteca Nacional Digital de México (c); n.d.).

For Oceanic Exchanges, the HNDM will participate with newspapers between 1800 and 1914, which is equivalent to 771 titles and 2,069,247 pages.

## Data and Metadata
The HNDM’s digitalization was obtained from 35mm microfilm rolls that the National Newspaper Library created. The publication’s stills have been reduced 21 times relative to their original size and contain between 140 and 180 line pairs per millimeter (pl/mm). This reduces the effects due to time on paper and ink tones from the original documents and produces a better contrast. 

To create the HNDM collection every page of every item from the newspaper was digitized in a bitonal TIFF image, and OCR was used to obtain text. This is stored in XML format that also includes descriptive metadata of the publications as well as metadata for the coordinates of each word on the page.

According to an analysis by the Dirección General de Cómputo y de Tecnologías de Información y Comunicación at UNAM (the National University’s Computing and Communication and Information Technologies General Office), the OCR average success rate, in the XML, is 54%. On the image’s readability, it was found that 72% have good readability, about 15% is regular, and 13% is bad. Their quality was 56% good, 34% regular, and less than 10% bad.

The dataset’s XML archive works with three metadata schemes (Dublin Core, custom OCR/XML Data, and Metadata Encoding & Transmission Standard) in a METS metadata scheme that includes, at the beginning of the file, a publication’s description in Dublin Core with: date, title, city, state, country, category, collection and language. It’s followed by an OCR structure that divides the page’s content in columns, regions, paragraphs, lines, and words with an associated coordinate. XML are in a MongoDB v.3.6 database, which works with the objects of: publication, item, page, collection, and publication’s description.

## References

Curiel, G., & Jimenez, R. J. (2015). Diez años de la Hemeroteca Nacional Digital de México. Breve reseña de una larga gestión de preservación y acceso, 2002-2012 en I Textos, pixeles y bits: Reflexiones sobre la publicación digital. Retrieved December 19, 2017, from [http://www.hndm.unam.mx/files/acerca-de-hndm/diez-anios-de-la-hemeroteca-nacional-digital-de-mexico.pdf](http://www.hndm.unam.mx/files/acerca-de-hndm/diez-anios-de-la-hemeroteca-nacional-digital-de-mexico.pdf)

Hemeroteca Nacional Digital de México (a). (n.d.). Antecedentes. Retrieved December 19, 2017, from [http://www.hnm.unam.mx/index.php/quienes-somos/antecedentes](http://www.hnm.unam.mx/index.php/quienes-somos/antecedentes)

Hemeroteca Nacional Digital de México (b).  (n.d.).Acerca de HNDM, Retrieved December 19, 2017, from   [http://www.hndm.unam.mx/index.php/es/acerca-de-hndm](http://www.hndm.unam.mx/index.php/es/acerca-de-hndm)

Hemeroteca Nacional Digital de México (c).  (n.d.).Fondos, Retrieved December 19, 2017, from [http://www.hnm.unam.mx/index.php/hemeroteca-nacional-de-mexico/colecciones/fondo-reservado/hemeroteca-nacional-digital-mexico](http://www.hnm.unam.mx/index.php/hemeroteca-nacional-de-mexico/colecciones/fondo-reservado/hemeroteca-nacional-digital-mexico)

# <a name="espanol"></a>Hemeroteca Nacional Digital de México

## Historia de la colección
La Hemeroteca Nacional Digital de México (HNDM) se crea entre 2004 y 2008.  A la par que las bibliotecas más importantes del mundo, se resolvió usar nuevos métodos de almacenamiento digital con el propósito de preservar la vida útil del material y aprovechar las ventajas de la era digital. 

El proyecto se enfoca en digitalizar la colección de microfilmes de la Hemeroteca Nacional de México conformado desde 1960. Utilizando la metodología que la Hemeroteca Nacional desarrolló para la creación del archivo microfilmado, se seleccionaron documentos según: el estado físico de las publicaciones, la demanda de consulta y la importancia histórica, patrimonial, periodística y documental. De esta forma, se ofrecen nuevos soportes para la manipulación de fuentes históricas y es posible realizar búsqueda por palabras, frases, año o periodos. 

## Composición de la colección
Hoy en día, la HNDM cuenta con casi ocho millones de páginas digitalizadas, 941 títulos de periódicos de 1722 a 2006. De estos 516 títulos (1722-1889) son de libre acceso y 425 (1890-2006) con acceso restringido que solo pueden consultarse dentro de las instalaciones de la Hemeroteca Nacional. 

Los acervos en microfilm y digital se encuentran dentro de la colección del Fondo Reservado de la Hemeroteca Nacional el cual contiene: “publicaciones periódicas mexicanas de 1722 a 1917; publicaciones periódicas extranjeras de 1665 a 1920; fondo García Valseca; Misceláneas hemerográficas y microfilmes de importantes periódicos” (Hemeroteca Nacional Digital de México (c); n.d.)

Para el proyecto de Oceanic Exchanges la HNDM participará con los periódicos de 1800 a 1914, que equivale a 771 títulos y 2,069,347 páginas.

## Datos y metadatos
La digitalización de la HNDM se obtuvo a partir de rollos de microfilm que la Hemeroteca Nacional generó en formato de 35mm. Los fotogramas de las publicaciones están reducidas 21 veces respecto al tamaño original y contienen entre 140  y 180 pares de líneas  por  milímetro  (pl/mm). Esto disminuye los efectos ocasionados por el paso del tiempo en los tonos del papel y las tintas del documento original y, a su vez, permite resaltar el contraste  real  de  los  documentos. 

Para la construcción de la HNDM se digitalizó cada página de cada item del periódico en una imagen TIFF bitonal, a la cual se les aplicó reconocimiento óptico de caracteres (OCR por sus siglas en inglés) para obtener el contenido textual almacenado en un formato XML, este contempla metadatos descriptivos de la publicación y metadatos que permiten obtener la ubicación de cada palabra contenida en el texto con respecto a la imagen TIFF.

Según un estudio de la Dirección General de Cómputo y de Tecnologías de Información y Comunicación de la UNAM, el nivel de acierto promedio del OCR, contenido en los archivos XML, es del 54%. En cuanto a la legibilidad de las imágenes, se encontró que el 72% tiene una buena calidad, casi el 15% es regular y un 13% es mala. En lo que respecta a la calidad de éstas, el 56% es buena, el 34% regular y menos del 10% es mala. 

Los archivos XML de la muestra manejan tres esquemas de metadatos (Dublin Core, Custom OCR XML Data y Metadata Encoding & Transmission Standard) en un esquema de metadatos METS que contempla al inicio del archivo una descripción de la publicación en Dublin Core con los datos: fecha, título, ciudad, estado, país, categoría, colección e idioma; seguida de una estructura para el OCR que divide el contenido de la página en columnas, regiones, párrafos, líneas y palabras, en donde cada palabra tiene asociadas unas coordenadas.

Todas las imágenes y sus correspondientes XML se encuentran cargados en una base de datos en MongoDB versión 3.6, la cual maneja los objetos de: publicación, ítem, página, colección y descripción de la publicación.

La Hemeroteca Nacional Digital de México, cuya plataforma está disponible desde el 2011 al público general, junto con la Hemeroteca Nacional se ha convertido en el principal repositorio documental del país.

## Referencias
Curiel, G., & Jimenez, R. J. (2015). Diez años de la Hemeroteca Nacional Digital de México. Breve reseña de una larga gestión de preservación y acceso, 2002-2012 en I Textos, pixeles y bits: Reflexiones sobre la publicación digital. Retrieved December 19, 2017, from [http://www.hndm.unam.mx/files/acerca-de-hndm/diez-anios-de-la-hemeroteca-nacional-digital-de-mexico.pdf](http://www.hndm.unam.mx/files/acerca-de-hndm/diez-anios-de-la-hemeroteca-nacional-digital-de-mexico.pdf)

Hemeroteca Nacional Digital de México (a). (n.d.). Antecedentes. Retrieved December 19, 2017, from [http://www.hnm.unam.mx/index.php/quienes-somos/antecedentes](http://www.hnm.unam.mx/index.php/quienes-somos/antecedentes)

Hemeroteca Nacional Digital de México (b).  (n.d.).Acerca de HNDM, Retrieved December 19, 2017, from   [http://www.hndm.unam.mx/index.php/es/acerca-de-hndm](http://www.hndm.unam.mx/index.php/es/acerca-de-hndm)

Hemeroteca Nacional Digital de México (c).  (n.d.).Fondos, Retrieved December 19, 2017, from [http://www.hnm.unam.mx/index.php/hemeroteca-nacional-de-mexico/colecciones/fondo-reservado/hemeroteca-nacional-digital-mexico](http://www.hnm.unam.mx/index.php/hemeroteca-nacional-de-mexico/colecciones/fondo-reservado/hemeroteca-nacional-digital-mexico)
