<template>
  <MyBox class="app-info">
    <MyParag class="app-info__parag">Barcha kinolar soni: 0</MyParag>
    <MyParag class="app-info__parag">Favourite kinolar soni: 0</MyParag>
    <MyParag class="app-info__parag">Liked kinolar soni: 0</MyParag>
  </MyBox>
</template>

<script>
import MyBox from "@/components/ui-components/MyBox.vue";
import MyParag from "@/components/ui-components/MyParag.vue";
export default {
  name: "MyBox",
  components: { MyBox, MyParag },
};
</script>

<style>
.app-info__parag {
  font-size: 22px;
  margin: 1.2rem 0;
}
</style>
