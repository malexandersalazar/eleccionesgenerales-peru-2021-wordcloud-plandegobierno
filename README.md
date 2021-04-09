# Elecciones Generales de Perú de 2021

## Antecedentes

Las elecciones generales de Perú de 2021 se realizarán el 11 de abril de dicho año para elegir al presidente de la república, dos vicepresidentes de la misma, 130 congresistas de la República y 5 parlamentarios andinos para el período gubernamental 2021-2026

## Proceso

Este proyecto se desarrolló en Python 3.8.5 usando los paquetes **nltk**, **numpy**, **pandas**, **fitz**, **re**, **spacy**, **matplotlib**, **seaborn**, **datetime**, **PIL** y **wordcloud**.

### Adquisición de Datos

Obtuve el listado de candidatos a la presidencia y sus respectivos planes de gobierno descargándolos manualmente desde el sitio Voto Informado del Jurado Nacional de Elecciones del Gobierno de Perú [[1]].

### Transformación de Datos

Empecé empleando el módulo **spacy** para recuperar los sustantivos, verbos y nombres propios dentro de cada plan de gobierno para luego quedarme con las palabras con más de 3 caracteres y excluir las que representaban números. De las palabras recuperadas se excluyeron todas aquellas que se repetían demasiadas veces a modo de muletilla o por el diseño documento.

Luego de identificar las 3 palabras más comunes o importantes dentro de cada plan de gobierno, las junte y eliminé todas aquellas que se repetian más de 3 veces de entre todas ellas. Repetí este proceso  hasta que no se vuelvan a repetir más de 3 veces las 3 palabras más significativas.
 
Las palabras eliminadas fueron: 'ama', 'sua', 'llulla', 'quella', 'perú', 's/', 'si', 'año', 'años', 'país', 'peruano', 'https', 'gob', 'pe', 'p.','2020','2020a','2019', 'además', '2020.', '2018', '2020.', '--', 'así','2.','nº','1.','10','20','15','30','2017','100', '2020b', 'iii','según', 'http', 'pdf', '65', 'nacional', 'política', 'podemos', 'solo', 'sólo', 'ello', 'peruanos', 'mayor', '2021', 'fin', 'ley', 'plan', 'toda', 'todo', 'todas', 'todos', 'aquí', 'allá', 'entre', 'veces', 'menos', 'más', 'países', 'desarrollo', 'millones', 'mundo', 'salud', 'dejar', 'días', 'día', 'sistema', 'debe', 'objetivo', 'personas', 'propuesta', 'través' , 'tener', 'primeros', 'bibliografía', 'políticas', 'primero', 'segundo', 'tercero', 'covid-19', 'manera', 'pandemia', 'doctrina', 'gobierno', 'nivel', 'niveles', 'caso', 'probabilidades', 'proporcionan', 'poner', '.', 'pensión', 'forma', 'formas', 'particular', 'enfoque', 'indicador', 'gasto', 'falta', 'número', '2021-2026', 'www.somosperu.pe', 'partido', 'torre', 'catalina', 'victoria', 'gestión', 'educación', 'capítulo', 'unión', 'impulsaremos', 'promoveremos','servicios', 'programa', 'programas', 'población','indicadores','medidas','objetivos','mejorar','metas', '.gob.pe', '.pdf', 'plan de gobierno' y 'partido morado'.

## Resultados

![alt text](dist/Acción_Popular.jpg "Acción Popular")
Palabras clave: trabajar, honestidad, pensiones

![alt text](dist/Alianza_para_el_Progreso.jpg "Alianza para el Progreso")
Palabras clave: empresas, inversión, agua

![alt text](dist/Avanza_País.jpg "Avanza País")
Palabras clave: inversión, infraestructura, protección

![alt text](dist/Democracia_Directa.jpg "Democracia Directa")
Palabras clave: ministerio, presupuesto, instituto

![alt text](dist/Frente_Amplio.jpg "Frente Amplio")
Palabras clave: implementación, incremento, porcentaje

![alt text](dist/Fuerza_Popular.jpg "Fuerza Popular")
Palabras clave: pobreza, sector, acceso

![alt text](dist/Juntos_por_El_Perú.jpg "Juntos por El Perú")
Palabras clave: derechos, fortalecer, capacidades

![alt text](dist/Partido_Morado.jpg "Partido Morado")
Palabras clave: calidad, vida, acceso

![alt text](dist/Partido_Nacionalista_Peruano.jpg "Partido Nacionalista Peruano")
Palabras clave: proyectos, reforma, fortalecer

![alt text](dist/Partido_Popular_Cristiano.jpg "Partido Popular Cristiano")
Palabras clave: derechos, convención, humanos

![alt text](dist/Perú_Libre.jpg "Perú Libre")
Palabras clave: empresas, sociedad, recursos

![alt text](dist/Perú_Patria_Segura.jpg "Perú Patria Segura")
Palabras clave: justicia, derechos, infraestructura

![alt text](dist/Podemos_Perú.jpg "Podemos Perú")
Palabras clave: creación, empresas, economía

![alt text](dist/Renovacion_Popular.jpg "Renovacion Popular")
Palabras clave: productos, calidad, zonas

![alt text](dist/Somos_Perú.jpg "Somos Perú")
Palabras clave: sector, porcentaje, recursos

![alt text](dist/Unión_Por_el_Perú.jpg "Unión Por el Perú")
Palabras clave: calidad, infraestructura, instituciones

![alt text](dist/Victoria_Nacional.jpg "Victoria Nacional")
Palabras clave: problemas, inversión, proyectos

## Bitácora

**2021-04-09.** Para la mayoría de los planes de gobierno, sus palabras clave consolidan los pensamientos del partido político o los dialogos y entrevistas que han compartido sus candidatos durante su campaña política. Sin embargo, tanto en el caso de **Renovación Popular** como en el de **Somos Perú**, sus palabras clave no expresan una orientación política clara.

## Disponibilidad de datos y materiales 

Los datos utilizados en el presente proyecto están disponibles a través del enlace [Voto Informado: Candidatos EG 2021](https://votoinformado.jne.gob.pe/voto/Home/ListaOP "Voto Informado: Candidatos EG 2021")

El modelo utilizado para el procesamiento de lenguaje natural esta diposnible a través del enlace [spaCy · Industrial-strength Natural Language Processing in Python](https://spacy.io/ "spaCy · Industrial-strength Natural Language Processing in Python")

## Referencias

1. Jurado Nacional de Elecciones - JNE. (s.f.). _Voto Informado: Candidatos EG 2021_. Gobierno del Perú. Recuperado el 8 de abril de 2021 de https://votoinformado.jne.gob.pe/voto/Home/ListaOP

[1]: https://votoinformado.jne.gob.pe/voto/Home/ListaOP