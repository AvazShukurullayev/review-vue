<template>
  <div id="app">
    <div class="container">
      <div class="contetn">
        <AppInfo />
        <div class="search-panel">
          <SearchPanel />
          <FilterButtons />
        </div>
        <MovieList />
        <MovieAddForm />
      </div>
    </div>
  </div>
</template>

<script>
import AppInfo from "@/components/app-info/AppInfo.vue";
export default {
  name: "App",
  components: {
    AppInfo,
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  .container {
    max-width: 1140px;
    width: 100%;
    margin: 0 auto;
    padding: 0 15px;
  }
}
</style>
