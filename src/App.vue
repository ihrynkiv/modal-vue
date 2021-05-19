<template>
  <the-header title="Learning Vue" />
  <the-resources />
</template>

<script>
import TheHeader from './components/layouts/TheHeader.vue';
import TheResources from './components/learning-resources/TheResources';
export default {
  components: {
    TheHeader,
    TheResources
  },
  provide: {
    storedResources: [
      {
        id: 'official-guide',
        title: 'Official guide',
        description: 'The official Vue.js documentation.',
        link: 'https://vuejs.org'
      },
      {
        id: 'google',
        title: 'Google',
        description: 'Learn to google.',
        link: 'https://google.com'
      }
    ]
  }
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

* {
  box-sizing: border-box;
}

html {
  font-family: 'Roboto', sans-serif;
}

body {
  margin: 0;
}
</style>
