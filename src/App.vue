<script setup>
import top from './components/header.vue'
import genprops from './components/genreprops.vue'
import comment from './components/comment.vue'
import foot from './components/footer.vue'
import listRec from './components/listRec.vue'

var genrelist = ['action','adventure']
let recomendation = [
  {
    mangaid: "1",
    name: "To Be Power",
    desc: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa consectetur, consequatur velit, aliquid praesentium quo inventore at et, eligendi quod commodi modi quas ipsum repellendus aperiam facilis ut adipisci ratione." ,
    image: "./src/image/idk.png",
    genrelist: ['action', 'adventure']
  },
  {
    mangaid: "1",
    name: "To Be Power",
    desc: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa consectetur, consequatur velit, aliquid praesentium quo inventore at et, eligendi quod commodi modi quas ipsum repellendus aperiam facilis ut adipisci ratione." ,
    image: "./src/image/idk.png",
    genrelist: ['action', 'adventure']
  }
]
let inputbutton = false
function input() {
  inputbutton =! inputbutton
  console.log(inputbutton)
}

function Screeen(id) {
  console.log(id)
  var mainScreen = document.getElementById('main');
  if(mainScreen.className == "hidden"){
    mainScreen.className = "block";
  } else {
    mainScreen.className = "hidden"
  }
  // var element = document.getElementById('flexOrNot')
  // if (element.className == "flex flex-row md:flex-col") {
  //   console.log("anjir");
  //   element.className = "flex flex-cols-1 md:flex-col";
  // } else {
  //   element.className = "flex flex-row md:flex-col";
  // }
}

</script>

<template>

<div class="mx-2 md:mx-32">
  <div>
    <top/>
  </div>


<div id="flexOrNot" class="flex flex-col">
  <div id="" class="flex">
    <template class="" v-for="list in recomendation">
    <div @click="Screeen(list.mangaid)" class="bg-gray-800 w-52 h-full py-2 pl-1 my-2 ml-1 rounded">
    <listRec 
      :mangaid="list.mangaid"
      :name="list.name"
      :desc="list.desc" 
      :image="list.image"
    />
    <genprops
      v-for="item in list.genrelist" 
        :genre="item"
    />
    </div>
    </template>
  </div>

  <!-- main -->
  <div id="main" class="hidden">
  <div class="md:mx-32 mx-2">
    <div>
    <div class="flex flex-row">
      <img src="" class="h-32 w-65 rounded-sm object-scale-down object-center" alt="">
      <Div>
        <h1>To be Power</h1>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Pariatur aspernatur amet ea esse rerum tenetur necessitatibus earum iusto nesciunt nihil in dolores, quod ullam aliquid id laboriosam suscipit unde doloribus.</p>
        <p>Type</p>
        <p>Year</p>
      </Div>
    </div>
    <genprops/>
    </div>
    <comment class="mx-auto"/>
  </div>
  </div>
</div>
</div>

  <foot />
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat&display=swap');
body{
  font-family: 'Montserrat', sans-serif;
  background-color: 202020;
}


</style>