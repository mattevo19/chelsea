<script setup>
import { ref } from "vue"

const name = ref("")
const players = ref(["mount", "alonso", "mendy", "lukaku", "havertz", "kovacic", "kante"])

const addToPlayers = () => {
  players.value.push(name.value)
  name.value = ""
}
console.log()
</script>

<template>
  <ul>
    <li v-for="player in players">{{ player }}</li>
  </ul>

  <form @submit.prevent="addToPlayers">
    <input v-model.trim="name" type="text" placeholder="Add player" />
    <button>Add</button>
  </form>
</template>
