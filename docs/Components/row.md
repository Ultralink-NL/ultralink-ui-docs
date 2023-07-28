---
sidebar_position: 2
---

# ZRow

El componente ZRow se utiliza en el contexto de un componente padre (ZTable o similar) que proporciona el contexto gridColumns y el dato dataRow. Este componente puede contener componentes secundarios o slots para representar las celdas individuales de la fila y mostrar los datos de manera adecuada.

## Ejemplo de uso


```jsx title="ultralink-ui/components/table"
<template>
  <div>
    <ZTable :headers="gridHeaders" :data="gridData">
        <!-- Componentes o slots para representar las celdas -->
        <ZRow  v-for="row in arrayCustom" :key="row.id" :data="row">
          <!-- Aqui podrias agregar los componentes a usar dentro de cada ROW -->
        </ZRow>
          <!-- Agregar más celdas según sea necesario -->
    </ZTable>
  </div>
</template>

<script setup>
import { ZTable, ZRow }  from 'ultralink-ui/components/table';

const gridHeaders = [
  { width: '200px' },
  { width: '150px' },
  // ...
];

const gridData = [
  { id: 1, name: 'John Doe', age: 30 },
  { id: 2, name: 'Jane Smith', age: 25 },
  // ...
];
</script>

```

En este ejemplo, el componente ZRow se utiliza dentro del componente ZTable, y se proporcionan los datos de la fila mediante el uso de un array iterable. Las celdas individuales dentro de la fila pueden mostrar los datos correspondientes a través de las propiedades del objeto dataRow. Recuerda que en este ejemplo se utilizan datos de ejemplo, y puedes personalizar el contenido de las celdas según tus necesidades.