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
    <SearchInput @search-value="(event)=> search.value" @placeholder='Ingresa los datos a buscar' />
```

## Caso de uso

```jsx title="Search Input"
<template>
  <div>
    <SearchInput @search-value="(event)=> search.value" @placeholder='Ingresa los datos a buscar' />
  </div>
</template>

<script setup>
import { ref } from 'vue'
import SearchInput from '@/components/SearchInput.vue'

const search = ref('')

const filteredSearch = computed(() => {
  let itemFiltered = customArray.value.filter(
    (data) => !search.value || data.itemName.toLowerCase().includes(search.value.toLowerCase())
  )
  return itemFiltered
})

</script>


```