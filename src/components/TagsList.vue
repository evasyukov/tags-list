<template>
    <div class="tags-list">
      <div v-for="(tag, index) in tags" :key="index" >
        
        {{ tag.text }}
        <v-icon v-if="tag.icon" class="tag-icon">{{ tag.icon }}</v-icon>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      align: String,
      tags: Array
    },
  };
  </script>
  
  <style lang="scss" scoped>
  .tags-list {
    margin-bottom: 100px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  
    .tag-item {
      display: inline-flex;
      align-items: center;
      padding: 8px 12px;
      background-color: #e0e0e0;
      border-radius: 16px;
      margin-right: 10px;
      transition: background-color 0.3s;
  
      &.align-left {
        justify-content: flex-start;
      }
  
      &.align-center {
        justify-content: center;
      }
  
      &:hover {
        background-color: darken(#e0e0e0, 5%);
      }
  
      .tag-icon {
        margin-left: 6px;
      }
    }
  }
  </style>
  