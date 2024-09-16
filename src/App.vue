<script>
export default {
  data() {
    return {
      name: 'Vue v3',
      status: true,
      languages: ['HTML', 'css', 'js', 'php', 'vue'],
      link: 'https://www.google.com'
    };
  },
  methods: {
    change_status() {
      if (this.status == true) {
        this.status = false;
      } else if (this.status == false) {
        this.status = true;
      } else {
        this.status = true
      }
    }
  }
};
</script>

<template>
  <!-- just view -->
  <h1>Hi! I'm {{ name }}.</h1>

  <!-- conditonal -->
  <p v-if="status">User is Active!</p>
  <p v-else>User is Inactive!</p>
  <hr />

  <!-- loop -->
  <h3>My Languages:-</h3>
  <ol>
    <li v-for="item in languages" :key="item">{{ item }}</li>
  </ol>

  <!-- link -->
  <!-- <a v-bind:href="link">Google</a> -->
  <a :href="link">Google</a>
  <br/>

  <!-- on click -->
  <!-- <button v-on:click="change_status">Change Status</button> -->
  <button @click="change_status">Change Status</button>

</template>

<style scoped>
/*  */
</style>
