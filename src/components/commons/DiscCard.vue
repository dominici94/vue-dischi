<template>
    <div class="disc-card">
        <div class="img-container">
          <img :src="disc.poster" :alt="disc.title">
        </div>
        <h2>{{disc.title}}</h2>
        <h3>{{disc.author}}</h3>
        <h3>{{disc.year}}</h3>
    </div>
</template>

<script>
export default {
    name : 'DiscCard',
    props : {
        disc : Object
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/partials/variables.scss';

    .disc-card{
        width: calc(100% / 5 - 30px);
        margin: 10px 15px;
        padding: 10px;
        background-color: $primaryColor;
        text-align: center;
        display: flex;
        flex-direction: column;
        align-items: center;
        color: white;

        .img-container{
          height: 150px;
          width: 150px;
          margin: 25px 0;
        }
          img{
            width: 100%;
          }

        h2{
          text-transform: uppercase;
          padding: 10px 0;
        }
        h3{
          color: gray;
          font-weight: lighter;
        }
    }
</style>