<template>
    <div class="wrapper">
      <keep-alive>
        <router-view :foods = "foods"></router-view>
      </keep-alive>
    </div>
</template>

<script>
const ERR_OK = 0;
export default {
  data () {
    return {
      foods: []
    };
  },
  created () {
    this.$http.get('/api/foods').then((response) => {
      response = response.body;
      if (response.errno === ERR_OK) {
        this.foods = response.data;
      }
    });
  }
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fff;
}
@charset "utf-8";
body{
  font-size: .12rem;
  font-family: "微软雅黑","Microsoft YaHei", Arial, SimHei;
}
.recommend-wrapper{
  padding-bottom: .42rem;
}
.recommend-wrapper h3{
  margin-left: .09rem;
  line-height: .34rem;
  font-size: .15rem;
  border-bottom: 1px solid #dfdfdf;
}
/*适配*/
@media only screen and (min-width: 321px) and (max-width: 360px) {
  html {font-size: 703%;}
}
@media only screen and (min-width: 361px) and (max-width: 413px) {
  html {font-size: 732%;}
}
@media only screen and (min-width:414px) and (max-width: 640px) {
  html {font-size: 808%;}
}
@media only screen and (width: 384px) {
  html {font-size: 750%;}
}
@media only screen and (width: 411px) {
  html {font-size: 800%;}
}
@media only screen and (width: 412px) {
  html {font-size: 800%;}
}
@media only screen and (width: 435px) {
  html {font-size: 845%;}
}
@media only screen and (width: 600px) {
  html {font-size: 1170%;}
}
@media screen and (min-width:768px){
  html{font-size: 1500%;}
}
</style>
