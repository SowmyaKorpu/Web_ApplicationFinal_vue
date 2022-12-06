<template>
    <div id="standingTable" class="StandingsBox">
        <table>
            <thead>
    <tr>
        <th class="LargeTh">
            Team
        </th>
        <th class="smallTh">
            PCT
        </th>
        <th class="smallTh">
            Played
        </th>
        <th class="smallTh">
            Won/Lost/Drawn
        </th>
        <th class="smallTh">
            Recent Form
        </th>
        <th class="smallTh">
            Points
        </th>
    </tr>
</thead >
        <tr v-for="ranking in rankings" :key="ranking.points">
            <RankingRow :ranking="ranking"/>          
        </tr>
        </table>
    </div>
</template>

<script>
import RankingRow from "./RankingRow.vue"
export default{
    name:'RankingList',
    components:{
        RankingRow
    },
    props:{
        rankings: Array
    }
}
</script>

<style scoped>
.contact-details {
            background-color: #8FA6CB;
            padding-top: 5px;
            text-align: left;
            padding-left: 20%;
            padding-bottom: 5px;
        }
.headerbg {
            background-color: black;
            padding: 10px;
            color: white;
            font-size: 17px;
            font-weight: 500;
        }
.StandingsBox{
    background-color: aqua;
}
thead{
    background-color: black;
    color: aliceblue;
}
th{
    text-align: center;
    border: 1px solid rgb(190, 190, 190);
}
.smallTh{
    width: 400px;
    height: 60px;
}
.LargeTh{
    width: 800px;
    height: 60px;
}
table{
    border-collapse: collapse;
}
</style>