<template>
<the-header title="RememberMe"></the-header>
<the-resource></the-resource>
</template>

<script>

import TheResource from './components/learning-resources/TheResource.vue';
import TheHeader from './components/layouts/TheHeader.vue';
export default {
  components: {
    
    TheResource,TheHeader
  },
 
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