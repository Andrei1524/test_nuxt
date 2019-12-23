<template>
  <div>
    <h2>{{ this.post.title }}</h2>
  </div>
</template>


<script>
  export default {
    data() {
      return {
        id: this.$route.params.id
      }
    },
    computed: {
      post() {
        return this.$store.state.projects.all.find(project => project.id == this.id);
      }
    }
  }
</script>

<style>

</style>
