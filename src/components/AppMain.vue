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
  methods: {
    filterCategory() {
      axios
        .get("https://www.breakingbadapi.com/api/characters", {
          params: {
            category: this.store.selectedValue,
          },
        })
        .then((resp) => {
          this.store.characters = resp.data;
          console.log(resp);
        });
    },
  },
  created() {
    this.filterCategory();
  },
};
</script>

<template>
  <AppCategory @search="filterCategory" />
  <AppCharacters />
</template>

<style lang="scss" scoped></style>
