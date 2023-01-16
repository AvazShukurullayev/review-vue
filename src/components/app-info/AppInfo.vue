<template>
  <MyBox class="app-info">
    <MyParag class="fs-2">Barcha kinolar soni: {{ moviesLength }}</MyParag>
    <MyParag class="fs-4"
      >Favourite kinolar soni: {{ favouriteMoviesLength }}</MyParag
    >
    <MyParag class="fs-4">Liked kinolar soni: {{ likedMoviesLength }}</MyParag>
  </MyBox>
</template>

<script>
import MyBox from "@/components/ui-components/MyBox.vue";
import MyParag from "@/components/ui-components/MyParag.vue";
export default {
  name: "AppInfo",
  components: { MyBox, MyParag },
  props: ["moviesLength", "favouriteMoviesLength", "likedMoviesLength"],
};
</script>
<style></style>
