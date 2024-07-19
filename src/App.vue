<template>
  <div class="tags-list">
    <div class="tags-list_main">
      <TagsList :tags="tags" style="justify-content: flex-end" />
      <TagsList :tags="tags" />
      <TagsList :tags="tags" style="justify-content: flex-end; width: 50%" />
      <TagsList :tags="tags" style="justify-content: flex-start; width: 50%" />
    </div>

    <!-- <button class="tags-list_btn-add" @click="addTag">Добавить тег</button> -->
  </div>
</template>

<script>
import TagsList from "./components/TagsList.vue";

export default {
  name: "App",
  components: {
    TagsList,
  },
  data() {
    return {
      tags: [
        { text: "v-btn", icon: "mdi-watch" },
        { text: "v-checkbox" },
        { text: "v-menu", icon: "mdi-email" },
        { text: "v-btn", icon: "mdi-check" },
      ],
    };
  },
  methods: {
    addTag() {
      this.tags.push({ text: "Новый тег", icon: "mdi-plus" });
    },
  },
};
</script>

<style lang="scss">
.tags-list {
  height: 90vh;

  &_main {
    padding: 20px;
  }
}
</style>
