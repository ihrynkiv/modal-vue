<template>
  <ul>
    <learning-resource
      v-for="res in resources"
      :key="res.id"
      :title="res.title"
      :description="res.description"
      :link="res.link"
      :id="res.id"
      @delete="deleteResource"
    />
  </ul>
</template>

<script>
import LearningResource from './LearningResource.vue';
export default {
  inject: ['resources', 'deleteResource'],
  components: {
    LearningResource
  }
};
</script>

<style scoped>
ul {
  list-style: none;
  margin: 0;
  padding: 0;
  margin: auto;
  max-width: 40rem;
}
</style>
