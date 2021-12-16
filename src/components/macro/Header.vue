<template>
  <header>
      <img src="../../assets/img/logo-spotify.png" alt="logo spotify">
  </header>
</template>

<script>
export default {
    name : 'Header',
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/partials/variables.scss';

    header{
        background-color: $primaryColor;
        img{
            width: 100px;
            padding: 10px 30px;
        }
    }
</style>