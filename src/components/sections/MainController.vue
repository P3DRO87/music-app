<script setup>
import { onUnmounted, ref } from "vue";
import SelectionBtn from "../fragments/SelectionBtn.vue";

const kick = [...Array(4).keys()].map((n) => n + 1);

const bpm = 150;
const timePerBeat = 60000 / bpm;

const beatCount = ref(1);

const beatInterval = setInterval(() => {
   beatCount.value = beatCount.value % 4 === 0 ? 1 : beatCount.value + 1;
}, timePerBeat);

onUnmounted(() => clearInterval(beatInterval));
</script>

<template>
   <div :class="`main-controller rounded-4px`">
      <div class="container">
         <div class="row">
            <div class="col-sm-auto ms-auto">
               <SelectionBtn btnText="Drum machine" />
            </div>
         </div>
         <div class="track-steps mt-4">
            <div class="container">
               <div class="row">
                  <div class="col-lg-4">
                     <div class="btn-container">
                        <button class="controller-btn d-flex flex-column gap-2">
                           <span>Kick</span>
                           <span>K</span>
                        </button>
                     </div>
                  </div>
                  <div class="col-lg-8">
                     <div class="btn-container">
                        <div class="container">
                           <div class="row g-0 step-container">
                              <template v-for="step in kick">
                                 <div class="col-lg-3 mb-2 g-1">
                                    <div
                                       :class="`step ${
                                          step === beatCount ? 'active' : ''
                                       }`"
                                    ></div>
                                 </div>
                              </template>
                           </div>
                        </div>
                     </div>
                  </div>
               </div>
               <div class="row">
                  <div class="col-lg-4">
                     <div class="btn-container">
                        <button class="controller-btn d-flex flex-column gap-2">
                           <span>Snare</span>
                           <span>S</span>
                        </button>
                     </div>
                  </div>
                  <div class="col-lg-8">
                     <div class="btn-container">
                        <div class="container">
                           <div class="row g-0 step-container">
                              <template v-for="step in kick">
                                 <div class="col-lg-3 mb-2 g-1">
                                    <div
                                       :class="`step ${
                                          step === beatCount ? 'active' : ''
                                       }`"
                                    ></div>
                                 </div>
                              </template>
                           </div>
                        </div>
                     </div>
                  </div>
               </div>
               <div class="row">
                  <div class="col-lg-4">
                     <div class="btn-container">
                        <button class="controller-btn d-flex flex-column gap-2">
                           <span>Hihat</span>
                           <span>H</span>
                        </button>
                     </div>
                  </div>
                  <div class="col-lg-8">
                     <div class="btn-container">
                        <div class="container">
                           <div class="row g-0 step-container">
                              <template v-for="step in kick">
                                 <div class="col-lg-3 mb-2 g-1">
                                    <div
                                       :class="`step ${
                                          step === beatCount ? 'active' : ''
                                       }`"
                                    ></div>
                                 </div>
                              </template>
                           </div>
                        </div>
                     </div>
                  </div>
               </div>
               <div class="row">
                  <div class="col-lg-4">
                     <div class="btn-container">
                        <button class="controller-btn d-flex flex-column gap-2">
                           <span>Chord 1</span>
                           <span>C</span>
                        </button>
                     </div>
                  </div>
                  <div class="col-lg-8">
                     <div class="btn-container">
                        <div class="container">
                           <div class="row g-0 step-container">
                              <template v-for="step in kick">
                                 <div class="col-lg-3 mb-2 g-1">
                                    <div
                                       :class="`step ${
                                          step === beatCount ? 'active' : ''
                                       }`"
                                    ></div>
                                 </div>
                              </template>
                           </div>
                        </div>
                     </div>
                  </div>
               </div>
               <div class="row">
                  <div class="col-lg-4">
                     <div class="btn-container">
                        <button class="controller-btn d-flex flex-column gap-2">
                           <span>chord 1 -u</span>
                           <span>No key bound</span>
                        </button>
                     </div>
                  </div>
                  <div class="col-lg-8">
                     <div class="btn-container">
                        <div class="container">
                           <div class="row g-0 step-container">
                              <template v-for="step in kick">
                                 <div class="col-lg-3 mb-2 g-1">
                                    <div
                                       :class="`step ${
                                          step === beatCount ? 'active' : ''
                                       }`"
                                    ></div>
                                 </div>
                              </template>
                           </div>
                        </div>
                     </div>
                  </div>
               </div>
            </div>
         </div>
      </div>
   </div>
</template>
