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
          <SearchPanel @onSearch="onSearch" />
          <FilterButtons @onFilterButton="onFilterButton" />
        </MyBox>
        <MovieList
          :movies="onFilterButtonHandler(onSearchHandler(movies, term), filter)"
        />
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
        {
          title: "Amir Temur",
          viewers: 811,
          favourite: false,
          like: false,
          id: 4,
        },
        {
          title: "Empire of Mogul",
          viewers: 1428,
          favourite: false,
          like: false,
          id: 5,
        },
        {
          title: "Murad IV. Bagdad Fatihi",
          viewers: 2455,
          favourite: false,
          like: false,
          id: 6,
        },
      ],
      term: "",
      filter: "all",
    };
  },
  methods: {
    onFilterButtonHandler(arr, filter) {
      switch (filter) {
        case "popular":
          return arr.filter((c) => c.favourite);
        case "mostViewers":
          return arr.filter((c) => c.viewers > 500);
        default:
          return arr;
      }
    },
    onFilterButton(param) {
      this.filter = param;
    },
    onSearch(param) {
      this.term = param;
    },
    onSearchHandler(arr, term) {
      if (term.length == 0) {
        return arr;
      }
      return arr.filter((c) =>
        c.title.toLowerCase().includes(term.toLowerCase())
      );
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
