<template>
  <MyBox>
    <ul class="list-group">
      <MyMovieItem
        v-for="movie in movies"
        :key="movie.id"
        :movie="movie"
        @onLike="$emit('onLike', $event)"
        @onFavourite="$emit('onFavourite', $event)"
        @onRemove="$emit('onRemove', $event)"
      />
    </ul>
  </MyBox>
</template>

<script>
import MyBox from "@/components/ui-components/MyBox.vue";
import MyMovieItem from "@/components/ui-components/MyMovieItem.vue";
export default {
  name: "MovieList",
  components: {
    MyBox,
    MyMovieItem,
  },
  props: ["movies"],
};
</script>

<style></style>
