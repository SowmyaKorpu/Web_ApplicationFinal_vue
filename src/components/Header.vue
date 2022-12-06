<template>
<div id="home" class="Navigation">
    <nav class="navbar">
     <div>
       <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSLcG--kAxMkGSMNeZ7p6-V3JpSuHng5XNE-w&usqp=CAU"  style="width:0px height:9px"/>
     </div>
     <ul class="nav-links">
       <div class="menu">
         <li><a href="#home">Home</a></li>
         <li><a href="#standingTable">Rankings</a></li>
         <li><a href="#contact">Contact</a></li>
       </div>
     </ul>
   </nav>
</div>
</template>

<script>

export default{
    name:'MyHeader',
    props:{ title:{type: String, default: "My app title"},
            author:{type: String, default: "Author Name"}

    },
    methods:{
        onClick(){
            console.log("We just clicked")
        }
    }
}

</script>
<style scoped>
.Navigation{
    size: 1vmax;
}
li {
 list-style: none;
}
.navbar {
 display: flex;
 align-items: center;
 justify-content: space-between;
 padding: 20px;
 background-color: rgb(36, 138, 138);
 color: #fff;
}
.nav-links a {
 color: #fff;
}
.menu {
 display: flex;
 gap: 1em;
 font-size: 18px;
}
.menu li:hover {
 background-color: #187e7e;
 border-radius: 5px;
 transition: 0.3s ease;
}
.menu li {
 padding: 5px 14px;
}
</style>
