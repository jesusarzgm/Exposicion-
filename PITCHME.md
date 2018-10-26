
### ORDENAMIENTO MERGE SORT ###

![Flux Explained](https://idea-instructions.com/merge-sort.png)

---
__Es una algoritmo de ordenamiento por mezcla, mejor conocido como "Merge Sort"
  de ordenamiento externo estable basado en la técnica divide y vencerás, tambien llamado 
  de intercalacion o combinacion, ya que intercala dos estructuras previamente ordenadas.__
 
 
![Flux Explained](https://upload.wikimedia.org/wikipedia/commons/thumb/c/cc/Merge-sort-example-300px.gif/220px-Merge-sort-example-300px.gif)
---
*** Ventajas ***

 * >Se evitan los problemas de intercambio de colaves en la manipulación de datos.
 * >Es efectivo para conjuntos de datos que se pueden aceder secuencialmente como arreglos, vectores y listas 
   ligadas. 
   
---
*** Desventajas ***

* > Está definido recursivamente y su implementación no recursiva emplea una pila, por lo que requiere un espacio adicional de memoria para almacenarla. 

* > No pertenece a la familia denominada "IN-SITU" que realizan el proceso de ordenamiento dentro del mismo vector. Ya que este no utiliza el espacio sobre el que están almacenados los datos sino que para poder funcionar requiere de un espacio de mamroia adicional del tamaño  de los datos a ordenar en el cual se realizan las mezclas.

---
### Ejemplo ###
