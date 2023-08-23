# Rounded Filter

Importa el componente desde la siguiente ruta:
```jsx
import RoundedFilter from '@/components/RoundedFilter.vue'
```

El componente recibe 2 parametros **obligatorios**:
> * **itemList**: Recibe la **referencia** de un arreglo de objetos cuya longitud es indefinida, **es necesario que los objetos dentro del arreglo cuenten con 2 propiedades importantes** para su funcionamiento.
```json
    const navbarMenu = ref([
        {
            itemName:'name',
            isActive: true,
        }
    ])
```
* **activeItemChanged**:  Recibe un método que devuelve el **nombre del elemento activo actual** para poder manipularlo dentro del archivo donde el componente **RoundedFilter** esta siendo importado. 

```js
     <RoundedFilter @activeItemChanged="handleItem"/>

    ------------------------------
    //La función se debe de ver de la siguiente forma
    const activeItem = ref()

    function handleItem(itemName) {
      activeItem.value = itemName;
    }

```

## Caso de uso

```jsx title="RoundedFilter"
<template>
  <div>
    <RoundedFilter :itemList="navbarMenu" @activeItemChanged="handleItem"/>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import RoundedFilter from '@/components/RoundedFilter.vue'

const activeItem = ref()
const navbarMenu = ref([
    {
        itemName: 'Servicios',
        isActive: true,
    },
    {
        itemName: 'Facturacion',
        isActive: false,
    },
    {
        itemName: 'Tickets',
        isActive: false,
    },
    {
        itemName: 'Email',
        isActive: false,
    },
    {
        itemName: 'Documentos',
        isActive: false,
    },
    {
        itemName: 'Estadisticas',
        isActive: false,
    },
])

function handleItem(itemName) {
    activeItem.value = itemName;
}

</script>


```