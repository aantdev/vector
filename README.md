# Vector

Vector implementation in C (C99 compliant), as a single-file library

# Quickstart

Simply copy the `vector.h` into your project, and include it (`#include "vector.h"`)

To access the function definitions, also do `#define VECTOR_IMPLEMENTATION` before the include.

```c
#define VECTOR_IMPLEMENTATION
#include "vector.h"

int main(void) {
    vector_t* vector = init_vector();

    push_back(vector, "Hello \0, 7");
    push_back(vector, "World!\n\0", 8);

    insert(vector, 1, "beautiful \0", 11);

    printf("%s", (char*)at(vector, 0));
    printf("%s", (char*)at(vector, 1));
    printf("%s", (char*)at(vector, get_index(vector)));
}
```
