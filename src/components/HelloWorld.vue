<template>
  <div class="hello">
    <h1>{{ msg }}</h1>

    <h3>icons</h3>
    <ul  >
        <li v-for="(item,index) in iconsList" :key="index">
            <i class="material-icons">{{item.name}}</i>
        </li>

    </ul>
  </div>
</template>

<script>
import iconsData from '../assets/import-icons.js'
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data () {
    return {
      iconsList: iconsData.nameList
    }
  },
  mounted () {
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
