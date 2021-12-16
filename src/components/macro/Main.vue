<template>
  <main>
    <div class="container">
      <div class="discs-list">
        <DiscCard v-for="(disc, index) in discs" :key="index" :disc="disc"/>
      </div>
    </div>
  </main>
</template>

<script>
import axios from 'axios';
import DiscCard from '../commons/DiscCard.vue';

export default {
  name : 'Main',
  components : {
    DiscCard
  },
  data(){
    return{
      discs : []
    }
  },
  created() {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music')
    .then((response) => {
        // handle success
        this.discs = response.data.response;
    })
    .catch(function (error) {
        // handle error
        console.log(error);
    });
  }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/partials/variables.scss';

  main{
    background-color: $secondaryColor;
    padding: 100px 0;

    .discs-list{
      display: flex;
      flex-wrap: wrap;

    }
  }

</style>