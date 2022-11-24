<template>
  <Amis :amisjson="amisjson"></Amis>
</template>
<script setup>
import Amis from './components/AmisRender.vue'
const amisjson={
    type: 'page',
    title: '表单页面',
    body: {
      type: 'form',
      mode: 'horizontal',
      api: '/saveForm',
      body: [
        {
          label: 'Name',
          type: 'input-text',
          name: 'name'
        },
        {
          label: 'Email',
          type: 'input-email',
          name: 'email'
        }
      ]
    }
  }
</script>
