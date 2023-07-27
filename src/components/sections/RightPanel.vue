<script setup>
import SelectionBtn from "../fragments/SelectionBtn.vue";
</script>

<template>
   <div class="right-panel rounded-4px">
      <h2 class="row-title">Row 2</h2>
      <div class="container">
         <div class="row justify-content-center">
            <p class="chord rounded-4px mb-3 w-auto">row w chorus</p>
            <p>Stored rows</p>
            <div class="col-lg-4">
               <p class="chord rounded-4px">Chord 1</p>
            </div>
            <div class="col-lg-4">
               <p class="chord rounded-4px">Chord 2</p>
            </div>
            <div class="col-lg-4">
               <p class="chord rounded-4px">Chord 3</p>
            </div>
         </div>
         <div class="row">
            <div class="col-lg-12 d-flex flex-column">
               <button class="rounded-4px">Add row</button>
               <button class="rounded-4px">Clear row</button>
            </div>
         </div>
         <div class="row">
            <div class="col-lg-12">
               <p class="text-center hihat-text">
                  <span class="bar"></span>
                  <span>hihat</span>
                  <span class="bar"></span>
               </p>
            </div>
         </div>
         <div class="row">
            <div class="col-lg-12 d-flex flex-column">
               <button class="rounded-4px">Save row</button>
               <button class="rounded-4px">Delete row</button>
               <button class="rounded-4px">Multiply row</button>
               <button class="rounded-4px">Divide width</button>
               <button class="rounded-4px">Duplicate</button>
            </div>
         </div>
         <div class="row mt-3">
            <div class="col-lg-12">
               <p>Type</p>
               <SelectionBtn btnText="Audio buffer" />
            </div>
         </div>
      </div>
   </div>
</template>
