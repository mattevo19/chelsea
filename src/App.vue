<script setup>
import Title from "./components/Title.vue"
import Badge from "./components/Badge.vue"
import { ref } from "vue"
import Form from "./components/Form.vue"

const name = ref("")
const players = ref(["mount", "alonso", "mendy", "lukaku", "havertz", "kovacic", "kante"])
const props = ref({
  title: "Chelsea",
  url: "https://1.bp.blogspot.com/-0oa9EtRDhwg/YDYNKk-Iv1I/AAAAAAAC5TA/8wr-e7py2E8wrJOoukbcNi8473L0CZRTgCNcBGAsYHQ/s1600/chelsea-2021-logo-erweiterung-von-footy-headlines.png"
})

const addToPlayers = (name) => {
  players.value.push(name)
}
</script>

<template>
  <Title :title="props.title" />
  <Badge :image="props.url" />

  <ul>
    <li v-for="player in players">{{ player }}</li>
  </ul>

  <form @submit.prevent="addToPlayers(name)">
    <input v-model.trim="name" type="text" placeholder="Add player" />
    <button>Add</button>
  </form>
</template>

<style>
@import "./assets/base.scss";
</style>
