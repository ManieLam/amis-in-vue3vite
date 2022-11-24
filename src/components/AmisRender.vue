<template>
  <div id="box"></div>
</template>

<script setup>
import { onMounted, defineProps } from "vue"
console.log("ces ");
const props= defineProps({
  amisjson: {
    type: Object,
    required: true
  }
})


onMounted(() => {
  // @ts-ignore
  var amis = amisRequire('amis/embed');
  console.log(amis);
  
  let amisScoped = amis.embed('#box', props.amisjson);
})

</script>
