
### ORDENAMIENTO MERGE SORT ###

![Flux Explained](https://idea-instructions.com/merge-sort.png)

---
__Es una algoritmo de ordenamiento por mezcla, mejor conocido como "Merge Sort"
  de ordenamiento externo estable basado en la técnica divide y vencerás, tambien llamado 
  de intercalacion o combinacion, ya que intercala dos estructuras previamente ordenadas.__
 
 
![Flux Explained](https://upload.wikimedia.org/wikipedia/commons/thumb/c/cc/Merge-sort-example-300px.gif/220px-Merge-sort-example-300px.gif)
---
*** Ventajas ***

 * Se evitan los problemas de intercambio de claves en la manipulación de datos.
 * Es efectivo para conjuntos de datos que se pueden aceder secuencialmente como arreglos, vectores y listas 
   ligadas. 
   
---
*** Desventajas ***

*  Está definido recursivamente y su implementación no recursiva emplea una pila, por lo que requiere un espacio adicional de memoria para almacenarla. 

*  No pertenece a la familia denominada "IN-SITU" que realizan el proceso de ordenamiento dentro del mismo vector. Ya que este no utiliza el espacio sobre el que están almacenados los datos sino que para poder funcionar requiere de un espacio de mamroia adicional del tamaño  de los datos a ordenar en el cual se realizan las mezclas.
---
### Funcionamiento ###
* Si la longuitud del array es menor o igual a 1 entonces ya esta ordenado 
* El array a ordenar se divide en dos mitades de tamaño similar 
* Cada mitad se ordena de forma recursiva aplicando el método MergeSort
* A continuación las dos mitades ya ordenadas se mezclan formando una secuencia ordenada 

---
### Ejemplo ###
![Flux Explained](https://data.whicdn.com/images/273495809/large.jpg)

---
```
public static void mergesort(int A[],int izq, int der){
    if (izq<der){
            int m=(izq+der)/2;
            mergesort(A,izq, m);
            mergesort(A,m+1, der);
            merge(A,izq, m, der);
    }
}
```

```
public static void merge(int A[],int izq, int m, int der){
   int i, j, k;
   int [] B = new int[A.length]; //array auxiliar
   for (i=izq; i<=der; i++) //copia ambas mitades en el array auxiliar
             B[i]=A[i];

             i=izq; j=m+1; k=izq;
             while (i<=m && j<=der) //copia el siguiente elemento más grande
             if (B[i]<=B[j])
                     A[k++]=B[i++];
             else
                     A[k++]=B[j++];
             while (i<=m) //copia los elementos que quedan de la
                           A[k++]=B[i++]; //primera mitad (si los hay)
 }
 ```
 
 ---
 
 >>>El tiempo de ejecución promedio del método MergeSort es (n log n)<<<
 
 ---
 ### Enlaces ###
 
* [GitHub](http://puntocomnoesunlenguaje.blogspot.com/2014/10/java-mergesort.html)
 
* [GitHub](https://es.wikipedia.org/wiki/Ordenamiento_por_mezcla)
---
