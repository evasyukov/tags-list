<template>
  <div class="tag"
  :class="{'align-left': align === 'left', 'align-center': align === 'center'}"
  >
    <div
      v-for="(tag) in tags"
      :key="tag"
      
    >
      {{ tag.text }}
      <v-icon v-if="tag.icon" class="tag-icon">{{ tag.icon }}</v-icon>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    align: String,
    tags: Array,
  },
};
</script>

<style lang="scss" scoped>
.tag {
  display: flex;
  justify-content: space-between;
  align-items: center;

  width: 800px;
  height: 100px;
  margin: auto;

  &-icon {
    margin-left: 6px;
  }
}
</style>
