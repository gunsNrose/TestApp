<template>
  <div>
    <a-button type="primary">hello world</a-button>
  </div>
</template>

<script>
  import { Button } from 'ant-design-vue';
  import https from '../https.js';
  export default {
    components:{ AButton:Button },
    name: 'App',
    data(){
      return{

      }
    },
    // fetch实现跨域
    created(){
      console.log('--1-');
      let params ={'name': 'lies', 'pwd': 'weyyywt'};
      let url = '/api/userInfo/login';
      https.fetchGet(url,params).then((data) => {
        console.log(data);
        localStorage.setItem('token', '');

      }).catch(err=>{
          console.log(err);
        }
      );
      console.log('---3');
    }
  }

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
