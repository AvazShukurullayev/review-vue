<template>
  <div class="btn-group">
    <button
      v-for="filterButton in filterButtons"
      type="button"
      class="btn"
      :class="[filter == filterButton.value ? 'btn-dark' : 'btn-outline-dark']"
      @click="getClickedValue(filterButton.value)"
    >
      {{ filterButton.title }}
    </button>
  </div>
</template>

<script>
export default {
  name: "FilterButtons",
  components: {},
  props: [],
  data() {
    return {
      filterButtons: [
        {
          title: "Barcha kinolar",
          value: "all",
        },
        {
          title: "Mashxur kinolar",
          value: "popular",
        },
        {
          title: "eng ko'p ko'rilgan kinolar",
          value: "mostViewers",
        },
      ],
      filter: "all",
    };
  },
  methods: {
    getClickedValue(param) {
      this.filter = param;
      this.$emit("onFilterButton", this.filter);
    },
  },
};
</script>

<style></style>
