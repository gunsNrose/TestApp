<template>
  <div>
    <a-button type="primary">wellcom to my home!</a-button>
  </div>
</template>

<script>
  import { Button } from 'ant-design-vue';

  export default {
    components:{ AButton:Button },
    name: 'App',
    data(){
      return{

      }
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
