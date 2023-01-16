<template>
  <input
    class="form-control mb-3"
    type="text"
    placeholder="Kinolarni qidirish..."
    v-model="searchedWord"
    @input="$emit('onSearch', searchedWord)"
  />
</template>

<script>
export default {
  name: "SearchPanel",
  components: {},
  data() {
    return {
      searchedWord: "",
    };
  },
};
</script>

<style></style>
