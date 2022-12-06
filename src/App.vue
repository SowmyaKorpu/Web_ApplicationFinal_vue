<template>
 <MyHeader title= "Cricket League Standings" author="Sowmya" />
 <RankingList :rankings="rankings"/>
 <MyFooter/>
</template>

<script>
import MyHeader from './components/Header.vue'
import RankingList from './components/RankingList.vue'
import MyFooter from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    MyHeader,
    RankingList,
    MyFooter
  },


data(){

  return{
    rankings:[]
  }

},


methods:{

  async fetchRanks(){
    const res = await fetch('https://webapplication-final.herokuapp.com/api')
    const data = await res.json()
    console.log(data)
    return data
    }
  },

  async created(){
  this.rankings = await this.fetchRanks()
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
body{
  margin: 0px;
  background-color: black;
}
</style>
