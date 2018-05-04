<template>
  <div class="hello">

  </div>
</template>

<script>
  import axios from 'axios'
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  methods:{
        test(){
          console.log("11111111shuai");
          axios({
            method:"get",
            url:'api/test/test'
          })
            .then(function (response) {
              console.log("11111111shuai",response);
            })
            .catch(function (error) {
              console.log(error);
            });
        }

  },
  mounted(){
    this.test()
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
