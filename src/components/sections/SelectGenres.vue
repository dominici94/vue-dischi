<template>
  <div class="select-genres">
      <form action="">
          <select v-model="selectVal" name="" id="" @change="$emit('select', selectVal)">
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

</style>