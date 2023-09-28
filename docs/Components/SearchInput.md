# Search Input

Importa el componente desde la siguiente ruta:
```jsx
import SearchInput from '@/components/SearchInput.vue'
```

El componente recibe 2 parametros: 

* **placeholder(opcional)**: Recibe el placeholder que se le quiere asignar al input.

* **search-value(obligatorio)**: Emite un evento que contiene los caracteres ingresados en el input (esta informacion puede ser recibida mediante una funcion flecha y almacenada en una variable reactiva).



El componente quedaria de esta manera:
```js
    <SearchInput @search-value="(event)=> search.value = event" @placeholder='Ingresa los datos a buscar' />
```

## NOTA
Es necesario proveer la variable reactiva search de la siguiente forma para el **buen funcionamiento** del componente.
```jsx title="Use provide"
import { provide } from 'vue'

const search = ref('')
provide('search',search)
```

## Caso de uso

```jsx title="Search Input"
<template>
  <div>
    <SearchInput @search-value="(event)=> search.value = event" @placeholder='Ingresa los datos a buscar' />
  </div>
</template>

<script setup>
import { ref, computed, provide } from 'vue'
import SearchInput from '@/components/SearchInput.vue'

const search = ref('')
provide('search',search)

const filteredSearch = computed(() => {
  let itemFiltered = customArray.value.filter(
    (data) => !search.value || data.itemName.toLowerCase().includes(search.value.toLowerCase())
  )
  return itemFiltered
})

</script>


```