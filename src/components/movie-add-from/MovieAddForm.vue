<template>
  <MyBox>
    <h2>Kino qo'shish</h2>
    <form class="d-flex">
      <input
        class="form-control"
        type="text"
        placeholder="Kinoni nomini kiriting"
        required
      />
      <input
        class="form-control"
        type="number"
        placeholder="Necha marotaba ko'rilgan"
        required
      />
      <button class="btn btn-outline-dark" type="submit">Qo'shish</button>
    </form>
  </MyBox>
</template>

<script>
import MyBox from "@/components/ui-components/MyBox.vue";
export default {
  name: "MovieAddForm",
  components: { MyBox },
};
</script>

<style></style>
