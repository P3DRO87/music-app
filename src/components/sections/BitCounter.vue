<script setup>
import { onUnmounted, ref } from "vue";

const props = defineProps({
   bpm: Number,
   compassCount: {
      default: 4,
   },
   boxShadowColor: String,
});

const bpm = props.bpm;
const timePerBeat = 60000 / bpm;

const compassItems = [...Array(props.compassCount).keys()].map((n) => n + 1);

const beatCount = ref(1);

const beatInterval = setInterval(() => {
   beatCount.value = beatCount.value % props.compassCount === 0 ? 1 : beatCount.value + 1;
}, timePerBeat);

onUnmounted(() => clearInterval(beatInterval));
</script>

<template>
   <div class="btn-container">
      <div class="container">
         <div class="row g-0 step-container">
            <template v-for="step in compassItems">
               <div class="col-lg-3 mb-2 g-1">
                  <div
                     :style="{
                        boxShadow: `${
                           step === beatCount && props.boxShadowColor
                              ? `1px 1px 8px 0px ${props.boxShadowColor}`
                              : ``
                        }`,
                     }"
                     :class="`step ${step === beatCount ? 'active' : ''}`"
                  ></div>
               </div>
            </template>
         </div>
      </div>
   </div>
</template>
