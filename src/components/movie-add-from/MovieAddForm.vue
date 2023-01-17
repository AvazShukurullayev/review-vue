<template>
  <MyBox>
    <h2 class="mb-2">Kino qo'shish</h2>
    <form class="d-flex" @submit.prevent="onSubmit">
      <input
        class="form-control"
        type="text"
        placeholder="Kinoni nomini kiriting"
        v-model="form.title"
        required
      />
      <input
        class="form-control"
        type="number"
        placeholder="Necha marotaba ko'rilgan"
        v-model="form.viewers"
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
  data() {
    return {
      form: {},
    };
  },
  methods: {
    onSubmit() {
      const newMovieItem = {
        title: this.form.title,
        viewers: this.form.viewers,
        like: false,
        favourite: false,
        id: Date.now(),
      };
      this.$emit("onSubmitHandler", newMovieItem);
      this.form = {};
    },
  },
};
</script>

<style></style>
