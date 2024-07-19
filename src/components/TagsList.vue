<template>
  <div class="tag">
    <div class="tag_item" v-for="tag in tags" :key="tag">
      {{ tag.text }}
      <v-icon v-if="tag.icon" class="tag-icon">{{ tag.icon }}</v-icon>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    tags: Array,
  },
};
</script>

<style lang="scss" scoped>
.tag {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  margin-bottom: 70px;

  &_item {
    padding: 0 5px;
  }
}
</style>
