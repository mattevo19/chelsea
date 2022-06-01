<script setup>
import { ref } from "vue"

import Title from "./components/Title.vue"
import Badge from "./components/Badge.vue"
import PlayerList from "./components/PlayerList.vue"

const props = ref({
  title: "Chelsea",
  url: "https://1.bp.blogspot.com/-0oa9EtRDhwg/YDYNKk-Iv1I/AAAAAAAC5TA/8wr-e7py2E8wrJOoukbcNi8473L0CZRTgCNcBGAsYHQ/s1600/chelsea-2021-logo-erweiterung-von-footy-headlines.png"
})
</script>

<template>
  <Title :title="props.title" />
  <Badge :image="props.url" />
  <PlayerList />
</template>

<style>
@import "./styles/base.scss";
</style>
