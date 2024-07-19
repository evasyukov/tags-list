<template>
  <div class="tags-list">
    <!-- <v-btn style="margin-top: 15px;" @click="addTag">Добавить тег</v-btn> -->

    <TagsList :tags="tags" :align="left"/>
    <TagsList :tags="tags" :align="center"/>
    <TagsList :tags="tags" :align="left"/>

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
        { text: "v-btn", icon: "mdi-watch"},
        { text: "текст2", icon: "mdi-check" },
        { text: "текст1", icon: "mdi-email" },
        { text: "текст1"},
        // { text: "текст2", icon: "mdi-check" },
        // { text: "текст1" },
        // { text: "текст2", icon: "mdi-check" },
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

<style lang="scss" scoped>
.tags-list {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  text-align: center;
  height: 100%;
}
</style>
