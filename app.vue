<template>
  <div>
    <WaveSurfer ref="refWaveSurfer" src="/demo.wav" peaks-data="/demo.json" :options="waveSurferOption"/>
    <button @click="play">play</button>
    <button @click="pause">pause</button>
  </div>
</template>
<script setup>
const waveSurferOption = {
  height: 340,
  progressColor: '#e03639',
  waveColor: '#e7e7e7',
  cursorColor: '#FFDDDD',
  barWidth: 2,
  mediaControls: false,
  backend: 'MediaElement',
  scrollParent:true,
  xhr: {
    mode: 'no-cors'
  }
}
const refWaveSurfer = ref(null);

function play() {
  refWaveSurfer.value.waveSurfer.play();
}

function pause(){
  refWaveSurfer.value.waveSurfer.pause();
}


</script>
