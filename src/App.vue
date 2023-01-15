<template>
  <div id="app">
    <div class="container font-monospace">
      <div class="content">
        <AppInfo />
        <MyBox class="search-panel">
          <SearchPanel />
          <FilterButtons />
        </MyBox>
        <MovieList />
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
