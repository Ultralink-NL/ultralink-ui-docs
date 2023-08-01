---
sidebar_position: 1
---

# ZTable

El componente ZTable se puede utilizar en otros componentes Vue proporcionando las propiedades headers y, opcionalmente, data y height. Es esencial proporcionar las headers para que la cuadrícula muestre correctamente los encabezados de las columnas.


## Ejemplo

```jsx title="ultralink-ui/components/table"
<template>
  <div>
    <ZTable :headers="gridHeaders" height="400px">
      <!-- Contenido adicional o slots aquí -->
    </ZTable>
  </div>
</template>

<script setup>
import { ZTable } from 'ultralink-ui/components/table'

const gridHeaders = [
  { value: 'id', width: '200px' }, // Definir más columnas según sea necesario
  { value: 'Name', width: '150px' },
  // ...
];

const gridData = [
  { id: 1, name: 'John Doe', age: 30 },
  { id: 2, name: 'Jane Smith', age: 25 },
  // ...
];

const sidebarDataToSend  = [
  {
    icon: 'fa-solid fa-plus',
    event: activeDialog
  },
  {
    icon: 'fa-regular fa-arrows-rotate'
  },
  {
    icon: 'fa-light fa-info'
  }
];


</script>

```

Este código mostraría una cuadrícula con las columnas y datos proporcionados, y tendría una altura de 400 píxeles. Se puede agregar contenido adicional dentro del componente ZGrid utilizando slots. Recuerda que el componente ZHeader mencionado en el código proporcionado se implementa de manera automatica al enviarle mediante props headers.


## Tabla con Sidebar

En este componente se puede utilizar un sidebar del lado derecho agregando la propiedad: **type** en la cual especificamos **"sidebar"** y tenemos que enviarle lo que contendra el sidebar con un array de objetos, en los cuales necesitas agregar las propiedades de **icon** con la clase del icono y el **event** para poder ejecutar una funcion en el click.

```jsx title="ultralink-ui/components/table"
<template>
  <div>
    <ZTable :headers="gridHeaders" height="400px" type="sidebar" :sidebarData="sidebarDataToSend">
      <!-- Contenido adicional o slots aquí -->
    </ZTable>
  </div>
</template>

<script setup>
import { ZTable } from 'ultralink-ui/components/table'

const gridHeaders = [
  { value: 'id', width: '200px' }, // Definir más columnas según sea necesario
  { value: 'Name', width: '150px' },
  // ...
];

const sidebarDataToSend  = [
  {
    icon: 'fa-solid fa-plus',
    event: activeDialog
  },
  {
    icon: 'fa-regular fa-arrows-rotate',
    event: syncData
  },
  {
    icon: 'fa-light fa-info'
    event: goToInfoPage
  }
]
</script>

```