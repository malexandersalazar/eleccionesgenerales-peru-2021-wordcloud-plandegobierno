# Elecciones Generales de Perú de 2021

## Antecedentes

Las elecciones generales de Perú de 2021 se realizarán el 11 de abril de dicho año para elegir al presidente de la república, dos vicepresidentes de la misma, 130 congresistas de la República y 5 parlamentarios andinos para el período gubernamental 2021-2026

## Proceso

Este proyecto se desarrolló en Python 3.8.5 usando los paquetes **nltk**, **numpy**, **pandas**, **fitz**, **re**, **spacy**, **matplotlib**, **seaborn**, **datetime**, **PIL** y **wordcloud**.

### Adquisición de Datos

Obtuve el listado de candidatos a la presidencia y sus respectivos planes de gobierno descargándolos manualmente desde el sitio Voto Informado del Jurado Nacional de Elecciones del Gobierno de Perú [[1]].

### Transformación de Datos

Empecé empleando el módulo **spacy** para recuperar los sustantivos, verbos y nombres propios dentro de cada plan de gobierno.

Luego me quedé con las palabras más representativas de cada uno suprimiendo las palabras con menos de 3 caracteres, las que representaban números y las que se repetían muchas veces a modo de muletilla o por el diseño del documento. Por ejemplo: 'ama', 'sua', 'llulla', 'quella', 'perú', 's/', 'si', 'año', 'años', 'país', 'peruano', 'https', 'gob', 'pe', 'p.','2020','2020a','2019', 'además', '2020.', '2018', '2020.', '--', 'así','2.','nº','1.','10','20','15','30','2017','100', '2020b', 'iii','según', 'http', 'pdf', '65', 'nacional', 'política', 'podemos', 'solo', 'sólo', 'ello', 'peruanos', 'mayor', '2021', 'fin', 'ley', 'plan', 'toda', 'todo', 'todas', 'todos', 'aquí', 'allá', 'entre', 'veces', 'menos', 'más', 'países', 'desarrollo', 'millones', 'mundo', 'salud', 'dejar', 'días', 'día', 'sistema', 'debe', 'objetivo', 'personas', 'propuesta', 'través' , 'tener', 'primeros', 'bibliografía', 'políticas', 'primero', 'segundo', 'tercero', 'covid-19', 'manera', 'pandemia', 'doctrina', 'gobierno', 'nivel', 'niveles', 'caso', 'probabilidades', 'proporcionan', 'poner', '.', 'pensión', 'forma', 'formas', 'particular', 'enfoque', 'indicador', 'gasto', 'falta', 'número', '2021-2026', 'www.somosperu.pe', 'partido', 'torre', 'catalina', 'victoria', 'gestión', '.gob.pe', '.pdf', 'plan de gobierno' y 'partido morado'.

## Resultados

![alt text](dist/Acción_Popular.jpg "Acción Popular")
Palabras clave: trabajar, honestidad, pensiones, reinstalar, reforma, acción, empresas

![alt text](dist/Alianza_para_el_Progreso.jpg "Alianza para el Progreso")
Palabras clave: empresas, inversión, agua, educación, recursos, proyectos, servicios

![alt text](dist/Avanza_País.jpg "Avanza País")
Palabras clave: inversión, infraestructura, servicios, programas, protección, corrupción, creación

![alt text](dist/Democracia_Directa.jpg "Democracia Directa")
Palabras clave: educación, población, ministerio, presupuesto, instituto, servicios, entidades

![alt text](dist/Frente_Amplio.jpg "Frente Amplio")
Palabras clave: implementación, medidas, educación, programa, incremento, porcentaje, recursos

![alt text](dist/Fuerza_Popular.jpg "Fuerza Popular")
Palabras clave: educación, servicios, pobreza, sector, población, programas, acceso

![alt text](dist/Juntos_por_El_Perú.jpg "Juntos por El Perú")
Palabras clave: derechos, educación, fortalecer, capacidades, género, servicios, participación

![alt text](dist/Partido_Morado.jpg "Partido Morado")
Palabras clave: servicios, calidad, educación, vida, acceso, instituciones, información

![alt text](dist/Partido_Nacionalista_Peruano.jpg "Partido Nacionalista Peruano")
Palabras clave: programa, población, proyectos, servicios, reforma, fortalecer, establecer

![alt text](dist/Partido_Popular_Cristiano.jpg "Partido Popular Cristiano")
Palabras clave: derechos, convención, humanos, discriminación, igualdad, pesem, persona

![alt text](dist/Perú_Libre.jpg "Perú Libre")
Palabras clave: programa, educación, empresas, capítulo, sociedad, recursos, sector

![alt text](dist/Perú_Patria_Segura.jpg "Perú Patria Segura")
Palabras clave: justicia, derechos, infraestructura, recursos, seguridad, calidad, sector

![alt text](dist/Podemos_Perú.jpg "Podemos Perú")
Palabras clave: educación, programa, creación, servicios, empresas, economía, recursos

![alt text](dist/Renovacion_Popular.jpg "Renovacion Popular")
Palabras clave: promoveremos, impulsaremos, productos, calidad, zonas, recursos, medio

![alt text](dist/Somos_Perú.jpg "Somos Perú")
Palabras clave: población, metas, servicios, indicadores, sector, porcentaje, recursos

![alt text](dist/Unión_Por_el_Perú.jpg "Unión Por el Perú")
Palabras clave: educación, unión, calidad, infraestructura, mejorar, instituciones, desarrollar

![alt text](dist/Victoria_Nacional.jpg "Victoria Nacional")
Palabras clave: objetivos, educación, problemas, indicadores, metas, servicios, inversión



## Disponibilidad de datos y materiales 

Los datos utilizados en el presente proyecto están disponibles a través del enlace [Voto Informado: Candidatos EG 2021](https://votoinformado.jne.gob.pe/voto/Home/ListaOP "Voto Informado: Candidatos EG 2021")

El modelo utilizado para el procesamiento de lenguaje natural esta diposnible a través del enlace [spaCy · Industrial-strength Natural Language Processing in Python](https://spacy.io/ "spaCy · Industrial-strength Natural Language Processing in Python")

## Referencias

1. Jurado Nacional de Elecciones - JNE. (s.f.). _Voto Informado: Candidatos EG 2021_. Gobierno del Perú. Recuperado el 8 de abril de 2021 de https://votoinformado.jne.gob.pe/voto/Home/ListaOP

[1]: https://votoinformado.jne.gob.pe/voto/Home/ListaOP