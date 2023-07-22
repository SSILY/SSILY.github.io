---
title: Primer post
date: 2023-07-21 13:22:00 -500
categories: [test,blog]
tags: [blogging,testing,markdown,jekyll]
---

## Esta es mi primera prueba publicando en el blog

```python
'''
Escribe un programa para leer mbox-short.txt Cuando encuentres una línea que comience con 'From' como la siguiente línea:

    From stephen.marquard@uct.ac.za Sat Jan  5 09:14:16 2008

Analiza la línea From utilizando split() e imprime la segunda palabra en la línea (es decir, la dirección completa de la persona que envió el mensaje). A continuación, imprime un recuento al final.

Sugerencia: asegúrate de no incluir las líneas que comienzan con 'From:'.
'''

#Creamos un manejador de archivo
manejador_archivo = open('mbox-short.txt')

#Creamos una lista
lista_correos = list()

#Creamos un contador
contador = 0

#Iteramos en el archivo
for linea in manejador_archivo:
    #Quitamos el salto de linea
    linea = linea.rstrip()
    #Partimos la cadena en palaras
    palabras = linea.split()

    #Guardian - Si la longitud de la lista es menor a 3 y no comienza con From SALTA ESA LINEA
    if len(palabras) < 3 or palabras[0] != 'From':
        continue
    #Añadimos el correo a la lista
    lista_correos.append(palabras[1])
    #Incrementamos el contador
    contador = contador + 1

#Mostramos el resultado iterando sobre la lista
for correo in lista_correos:
    print(correo)

#Impresion del contador
print('Hay', contador, 'lineas en el archivo con From como la primer palabra')
```

