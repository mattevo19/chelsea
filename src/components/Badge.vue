<script setup>
defineProps({
  image: String
})
</script>

<template>
  <img class="image" :src="image" />
</template>

<style>
.image {
  height: 100px;
}
</style>
