<template>
  <li class="list-group-item d-flex align-items-center justify-content-between">
    <span class="list-group-item__label">{{ movie.title }}</span>
    <div class="d-flex align-items-center">
      <input
        class="form-control list-group-item__input"
        type="text"
        placeholder="Necha marotaba ko'rilgan"
        :value="movie.viewers"
      />
      <button class="btn-cookie btn-sm">
        <i class="fas fa-cookie"></i>
      </button>
      <button class="btn-trash btn-sm">
        <i class="fas fa-trash"></i>
      </button>
      <i class="fas fa-star"></i>
    </div>
  </li>
</template>

<script>
export default {
  name: "MyMovieItem",
  components: {},
  props: ["movie"],
};
</script>

<style></style>
