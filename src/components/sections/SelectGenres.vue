<template>
  <div class="select-genres">
      <form action="">
          <select v-model="selectVal" name="" id="" @change="$emit('select', selectVal)">
              <option value="All">All</option>
              <option value="Rock">Rock</option>
              <option value="Pop">Pop</option>
              <option value="Jazz">Jazz</option>
              <option value="Metal">Metal</option>
          </select>
      </form>
  </div>
</template>

<script>
export default {
    name : 'SelectGenres',
    data(){
        return{
            selectVal : ''
        }
    }

}
</script>

<style lang="scss" scoped>
@import '../../assets/style/partials/variables.scss';

    .select-genres{
        padding: 30px;
        display: flex;
        justify-content: center;

        select{
            background-color: $primaryColor;
            color: white;
            padding: 10px 15px;
            border: 1px solid $secondaryColor;
            border-radius: 20px;
        }
    }
</style>