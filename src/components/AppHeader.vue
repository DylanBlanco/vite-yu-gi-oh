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
@use '../assets/scss/header.scss' as *;
</style>
