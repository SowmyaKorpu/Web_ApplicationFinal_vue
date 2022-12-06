<template>
<td class="TeamPicText" style="background-color:#DBE8D8"><img class="imageTexPad" v-bind:src= "ranking.teamImage" style="width:10px;height:10px;">{{ranking.teamName}}  <label v-if="ranking.qualified" style="text-align:right; color: green;"> Q</label></td>
<td style="background-color:#C3E0E5" >{{ranking.pct}}</td>
<td style="background-color:#d7d9f2">{{ranking.played}}</td>
<td style="background-color:#C3E0E5">{{ranking.results}}</td>
<td style="background-color:#d7d9f2">{{ranking.recentForm}}</td>
<td style="background-color:#C3E0E5">{{ranking.points}}</td>
</template>
<script>
export default{
    name:'RankingRow',
    props:{
        ranking: Array
    }
}

</script>

<style scoped>
.TeamPicText{
    text-align: left;
    padding-left: 10px;
}
.imageTexPad{
    padding-right: 20px;
}
td{
    padding: 10px;
    border: 1px solid rgb(190, 190, 190);
}
</style>