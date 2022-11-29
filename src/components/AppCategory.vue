<script>
import { store } from "../store.js";
export default {
  name: "selectedValue",
  data() {
    return {
      store,
    };
  },
};
</script>

<template>
  <section class="container pb-4 pl-3">
    <select
      class="form-select w-auto"
      v-model="store.selectedValue"
      aria-label="Default select example"
      @change="$emit('search')"
    >
      <option value="" selected>Select category</option>
      <option value="Breaking Bad">Breaking Bad</option>
      <option value="Better Call Saul">Better Call Saul</option>
    </select>
  </section>
</template>

<style lang="scss" scoped></style>
