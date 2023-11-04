# Day 2 OpenMP
* OpenMP is an interface that allows programmers to specify
parallelism without having to manage low-level details like thread
creation and low-level synchronization.
* OpenMP is a shared-memory multi-threading model
* OpenMP is a set of 
  * Compiler directives
  * Library routines and APIs
 
## Why OpenMP ? 
* Easier to use
* requires minimal changes to squential program


Sequental programes were not meant to run on multiple CPUs
** hello_world.cpp **
```
#include <iostream>

int main(){
    int id = 0;
    printf("Hello %d ", id);
    printf("World %d ", id);
}
g++ hello_world.cpp -o hello_world
```
** hello_world_parallel.cpp **
```
#include <iostream>
#include <omp.h>

int main(){

    #pragma omp parallel 
    {
        int id = omp_get_thread_num();
        printf("Hello %d ", id);
        printf("World %d ", id);
    }
}

g++ hello_world_parallel.cpp -fopenmp
```

## Shared-memory programming model 

## Data-Sharing: Reduction

