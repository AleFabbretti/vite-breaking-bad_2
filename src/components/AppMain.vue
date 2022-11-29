<script>
import axios from "axios";
import { store } from "../store.js";
import AppCategory from "./AppCategory.vue";
import AppCharacters from "./AppCharacters.vue";

export default {
  components: {
    AppCategory,
    AppCharacters,
  },
  data() {
    return {
      store,
    };
  },
  created() {
    axios.get("https://www.breakingbadapi.com/api/characters").then((resp) => {
      this.store.characters = resp.data;
      console.log(resp);
    });
  },
};
</script>

<template>
  <AppCategory />
  <AppCharacters />
</template>

<style lang="scss" scoped></style>
