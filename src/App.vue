<script setup>
import { reactive } from "vue";
import Header from "./components/sections/Header.vue";
import MainController from "./components/sections/MainController.vue";
import RightPanel from "./components/sections/RightPanel.vue";

const initialGame = Array(9).fill("");

const listOfGames = reactive([initialGame]);
</script>

<template>
   <Header />
   <main class="my-5">
      <div class="container">
         <div class="row">
            <div class="col-lg-8">
               <MainController />
            </div>
            <div class="col-lg-4">
               <RightPanel />
            </div>
         </div>
      </div>
   </main>
</template>
