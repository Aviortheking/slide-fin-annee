<script setup>
import {defineProps} from 'vue'

const props = defineProps({
  image: {
    type: String,
  }
})
</script>
<template>
  <div class="slidev-layout image">
    <div class="image-contaier">
      <img class="image-item" style="object-fit: contain" :src="props.image">
    </div>
    <div class="pl-40 my-auto w-full block">
      <slot/>
    </div>
  </div>
</template>
