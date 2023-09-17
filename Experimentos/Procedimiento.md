Procedimiento para la visualización de un plan de estudios basada en competencias

Pasos tanto en RStudio como en Gephi
- Excel > gravarlo com a CSV (las columnss han de ser competencuas y las filas assignaturas, en caso contrario hay que transponer la matriz en R aplicando el trans.awk)
- R > ejecutar script laia.R
  -- hay que editar a mano varias cosas (el nombre de archivo de entrada y de salida añadiendo “-jaccard”), esto genera un CSV nombre-jaccard.csv
  -- este CSV es necesario editarlo para quitarle las comillas dobles, quitar las V de las variables y añadir un punto y coma ‘;’ al principio de la primera línea
- Gephi > leerlo como undirected, Force atlas / Partition > Modularity

Pasos para visualizar en RStudio
- Descargar Excel com a CSV, se descargará la pestanya en la que estés mapa_net (* rotació pendent)
- mover el CSV a la carpeta R_treball
- Abrir Gengraf.R con R studio
- Sesión > Set working directory>Choose>Carpeta R_treball
- Cambiar el nombre del CSV en el código para que coincida com el que estamos trabajando (ojo si hay comas en los campos)
- Hacer Run run run hasta que hace Plot
- Sobre la línea de Plot hago Run hasta que lo damos por bueno
- Buscar la línea PESDIF y canviar el valor si se quieren valorar más las diferencias
- Export and Save as image

Pasos para visualizar en Gephi
- Previo a Gephi en un editor de texto
 -- Abrir el fichero CSV jaccard resultante del R studio con un editor de texto
 -- Quitar V y comillas
 -- Añadir ";" al principio de todo
  
- En Gephi 
 -- Abrir el fichero CSV
 -- Undirected
 -- Aplicar Force Atlas
 -- Aplicar la modularidad 0.75 y colorear según esta
 -- Medida de los nodos 20-30
 -- Para exportar:
  -- Ancho borde 1
  -- Color borde 50,50,50
  -- Opacidad 80
  -- Mostrar etiquetas
  -- Avenir 24
  -- No propocional
  -- Contorno 0
  -- El resto por defecto

