<template>
  <div class='project'>
    <div class='thumbnail' :style="{ backgroundImage: 'url(' + thumbnail + ')' }"></div>
    <h1>{{ title }}</h1>
    <p>{{ description }}</p>
  </div>
</template>

<style scoped>
.project {
  padding: 10px;
  margin: 10px;
  border: 1px solid #ccc;
  width: 300px;
  float: left;
}

.thumbnail {
  width: 100%;
  height: 200px;
  background-position: center;
  background-size: cover;
}
</style>

<script>
export default {
  props: ['title', 'description', 'thumbnail']
}
</script>
