<template>
  <div id="app">
    <div style="width: 800px; height: 200px;">
      <TagsList :tags="tags" />
    </div>

    <v-btn @click="addTag">Добавить тег</v-btn>
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
        { text: "v-btn" },
        { text: "текст2", icon: "mdi-check" },
        { text: "текст1", icon: "mdi-check" },
        { text: "текст2", icon: "mdi-check" },
        { text: "текст1" },
        { text: "текст2", icon: "mdi-check" },
      ],
    };
  },
  methods: {
    addTag() {
      this.tags.push({ text: "Новый тег", icon: "mdi-plus" });
    },
    removeTag(index) {
      this.tags.splice(index, 1);
    },
  },
};
</script>

<style lang="scss" scoped>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  text-align: center;
  height: 100%;
}
</style>
