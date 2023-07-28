---
sidebar_position: 1
---

# ZTable

El componente ZTable se puede utilizar en otros componentes Vue proporcionando las propiedades headers y, opcionalmente, data y height. Es esencial proporcionar las headers para que la cuadrícula muestre correctamente los encabezados de las columnas.


## Ejemplo

```jsx title="ultralink-ui/components/table"
<template>
  <div>
    <ZTable :headers="gridHeaders" :data="gridData" height="400px">
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
</script>

```

Este código mostraría una cuadrícula con las columnas y datos proporcionados, y tendría una altura de 400 píxeles. Se puede agregar contenido adicional dentro del componente ZGrid utilizando slots. Recuerda que el componente ZHeader mencionado en el código proporcionado se implementa de manera automatica al enviarle mediante props headers.