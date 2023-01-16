<template>
  <li
    class="list-group-item d-flex align-items-center justify-content-between"
    :class="{ favourite: movie.favourite, like: movie.like }"
  >
    <span class="list-group-item__label" @click="$emit('onLike', movie.id)">
      {{ movie.title }}
    </span>
    <div class="d-flex align-items-center">
      <input
        class="form-control list-group-item__input"
        type="text"
        placeholder="Necha marotaba ko'rilgan"
        :value="movie.viewers"
      />
      <button class="btn-cookie btn-sm" @click="$emit('onFavourite', movie.id)">
        <i class="fas fa-cookie"></i>
      </button>
      <button class="btn-trash btn-sm" @click="$emit('onRemove', movie.id)">
        <i class="fas fa-trash"></i>
      </button>
      <i class="fas fa-star"></i>
    </div>
  </li>
</template>

<script>
export default {
  name: "MyMovieItem",
  props: ["movie"],
  components: {},
};
</script>

<style>
.list-group-item__label {
  line-height: 35px;
  font-size: 20px;
  max-width: 550px;
  width: 100%;
  cursor: pointer;
}
.list-group-item__input {
  text-align: center;
  font-size: 18px;
}
.btn-cookie,
.btn-trash {
  margin: 3px;
  width: 35px;
  height: 35px;
  border: none;
  border-radius: 3px;
  background-color: rgba(212, 212, 212, 0.548);
}
.btn-cookie:hover,
.btn-trash:hover {
  background-color: rgb(197, 197, 197);
}
.btn-cookie {
  color: rgb(250, 217, 27);
}
.btn-trash {
  color: red;
}
.fa-star {
  width: 35px;
  color: rgb(250, 217, 27);
  transform: translateX(30px);
  opacity: 0;
  transition: all 0.25s;
}
.list-group-item.favourite .list-group-item__label,
.list-group-item.favourite .list-group-item__input {
  color: rgb(250, 217, 27);
}
.list-group-item.like .fa-star {
  opacity: 1;
  transform: translateX(0);
}
</style>
