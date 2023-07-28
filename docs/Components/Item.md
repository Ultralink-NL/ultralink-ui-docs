---
sidebar_position: 3
---

# ZItem

Estos componentes se pueden utilizar en otros componentes Vue para representar una tabla o lista con diferentes tipos de elementos. Los datos y tipos se pueden proporcionar dinámicamente o con datos estáticos según la necesidad de la aplicación.

## Ejemplo de uso


```jsx title="ultralink-ui/components/table"
<template>
  <div>
    <ZTable :headers="gridHeaders" :data="gridData">
        <!-- Componentes o slots para representar las celdas -->
        <ZRow  v-for="row in arrayCustom" :key="row.id" :data="row">
          <ZItem :data="optionsToSend" type="options" />
          <ZItem :data="row.count" type="counter" :color="itemColor" />
          <ZItem :data="row.status" type="status" />
          <ZItem type="custom">
            <!-- Contenido personalizado como slots o otros componentes -->
            <span>{{ customData.label }}</span>
            <button @click="handleButtonClick">Click Me</button>
          </ZItem>
          <ZItem :data="plainText" type="plain" />
        </ZRow>
    </ZTable>
  </div>
</template>

<script setup>
import { ZTable, ZRow, ZItem } from './ZTable.vue';

const optionsToSend = [ { value: 'editar', color: '#fffff', textColor: '#5959595', event: updateData }, /* ... */ ];

</script>


```

En este ejemplo, se utiliza el componente ZTable para agrupar varios elementos ZItem. Cada elemento **(ZItem)** representa diferentes tipos de contenido, incluidas opciones **(options)**, un contador **(counter)**, un estado **(status)**, contenido personalizado **(custom)** y texto simple **(text)**. Dependiendo del tipo proporcionado, el componente ZItem mostrará el contenido apropiado. Los datos y tipos se pueden personalizar según los requerimientos de la aplicación.

