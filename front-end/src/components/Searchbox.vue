<script>


export default {
  data() {
    return {
      searchQuery: ''
    };
  },
  methods: {
    gotoSearch() {
      if(this.searchQuery){
        this.$router.push({ path: '/Search', query: { q: this.searchQuery } });
      }
    }
  }
};
</script>

<template>
  <div class="search-box">
    <input type="text" v-model="searchQuery" placeholder="请输入关键词" class="search-box-input">
    <button class="search-box-button" @click="gotoSearch"><img src="../assets/image/search.png"></button>
  </div>
</template>

<style scoped>

</style>