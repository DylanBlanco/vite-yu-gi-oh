<script>
export default {
  data() {
    return { 
      message: 'Yu-Gi-Oh Api',
    }
  }
}
</script>

<template>
  <header>
    <h1>
      {{ message }}
    </h1>
  </header>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

header {
  background-color: $mainBgColor;
  text-align: left;
  padding: 20px 0;
}

h1 {
  color: $mainColor;
  padding: 0 20px;
}
</style>
