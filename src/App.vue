<template>
  <div id="app">
    <div class="container font-monospace">
      <div class="content">
        <AppInfo
          :moviesLength="movies.length"
          :favouriteMoviesLength="movies.filter((c) => c.favourite).length"
          :likedMoviesLength="movies.filter((c) => c.like).length"
        />
        <MyBox class="search-panel">
          <SearchPanel @onSearch="onSearchHandler" />
          <FilterButtons />
        </MyBox>
        <MovieList :movies="movies" />
        <MovieAddForm />
      </div>
    </div>
  </div>
</template>

<script>
import AppInfo from "@/components/app-info/AppInfo.vue";
import MyBox from "@/components/ui-components/MyBox.vue";
import SearchPanel from "@/components/search-panel/SearchPanel.vue";
import FilterButtons from "@/components/filter-buttons/FilterButtons.vue";
import MovieList from "@/components/movie-list/MovieList.vue";
import MovieAddForm from "@/components/movie-add-from/MovieAddForm.vue";
export default {
  name: "App",
  components: {
    AppInfo,
    MyBox,
    SearchPanel,
    FilterButtons,
    MovieList,
    MovieAddForm,
  },
  data() {
    return {
      movies: [
        {
          title: "Omar",
          viewers: 811,
          favourite: false,
          like: false,
          id: 1,
        },
        {
          title: "Empire of Osman",
          viewers: 1428,
          favourite: false,
          like: false,
          id: 2,
        },
        {
          title: "Ertugrul",
          viewers: 455,
          favourite: false,
          like: false,
          id: 3,
        },
      ],
      term: "",
    };
  },
  methods: {
    onSearchHandler(param) {
      this.term = param;
    },
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
