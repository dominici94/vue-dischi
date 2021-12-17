<template>
  <div class="select-genres">
      <form action="">
          <select name="" id="" @change.prevent="$emit('select', searchText)">
              <option value="">All</option>
              <option value="">Rock</option>
              <option value="">Pop</option>
              <option value="">Jazz</option>
              <option value="">Metal</option>

          </select>
      </form>
  </div>
</template>

<script>
export default {
    name : 'SelectGenres',
    data(){
        return{
            searchText : ''
        }
    }

}
</script>

<style lang="scss" scoped>

</style>