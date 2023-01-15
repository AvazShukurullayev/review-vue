<template>
  <MyBox class="app-info">
    <MyParag class="fs-2">Barcha kinolar soni: 0</MyParag>
    <MyParag class="fs-4">Favourite kinolar soni: 0</MyParag>
    <MyParag class="fs-4">Liked kinolar soni: 0</MyParag>
  </MyBox>
</template>

<script>
import MyBox from "@/components/ui-components/MyBox.vue";
import MyParag from "@/components/ui-components/MyParag.vue";
export default {
  name: "AppInfo",
  components: { MyBox ,MyParag},
};
</script>
<style></style>
