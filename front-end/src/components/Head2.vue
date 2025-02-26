<script>
import Searchbox from "../components/Searchbox.vue";
export default {
  name: 'Head2',
  components: {
    Searchbox
  }
}

</script>

<template>
  <div>
    <div class="title">
      <router-link to="/">
        <div class="title1">
          考试信息网
        </div>
        <div class="title2">
          Examination information network
        </div>
      </router-link>
      <Searchbox/>
    </div>
    <nav>
      <router-link to="/">首页</router-link>
      <router-link to="/ExaminationProgram">考试项目</router-link>
      <router-link to="/TestRegistration">考试报名</router-link>
      <router-link to="/ScoreQuery">成绩查询</router-link>
      <router-link to="/Preparation">备考方案</router-link>
    </nav>
  </div>
</template>

<style scoped>
@import "../assets/css/Head2.css";
</style>