<template>
  <Catalog/>
  <TeacherInfo/>
  <Comment/>
  <Subscribe/>
</template>

<script>
// import Home from './components/Home.vue'
import Catalog from './components/Catalog.vue'
import TeacherInfo from './components/DetailCourse/TeacherInfo.vue'
import Comment from './components/DetailCourse/Comment.vue'
import Subscribe from './components/Subscribe.vue'
export default {
  name: 'App',
  components: {
    // Home
    Catalog,TeacherInfo,Comment,Subscribe
  }
}
</script>

<style>
#app {
  font-family: Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #000000;
  margin-top: 0px;
}
body{
  margin: 0px;
  padding: 0px;
}
p{
  margin-bottom: 10px;
  margin-top:10px;
  font-size: 18px;
}
@media only screen and (max-width: 600px) {
  p{
  margin-bottom: 8px;
  margin-top:8px;
  font-size: 14px;
  }
  h1{
    font-size: 22px;
  }
  h2{
    font-size: 21px;
  }
  h3{
    font-size: 19px;
  }
  h4{
    font-size: 18px;
  }
  h5{
    font-size: 16px;
  }
}
</style>
