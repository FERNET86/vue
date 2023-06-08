<template>
    <table :style="{ color: color, background: 'lightgrey' }">
      <tr v-for="item in data" :key="item.id">
        <td>
          <img :src="item.imagen" :alt="item.nombre" width="100" height="100">
        </td>
        <td>{{ item.nombre }}</td>
        <td>{{ item.numero }}</td>
      </tr>
    </table>
  </template>
  
  <script>
  export default {
    name: "EquiposTabla",
    props: {
      data: {
        type: Array,
        required: true
      },
      color: {
        type: String,
        default: "black"
      }
    }
  };
  </script>
  