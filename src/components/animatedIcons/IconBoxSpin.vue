<template>
  <svg
    @click="hdlAnimation"
    xmlns="http://www.w3.org/2000/svg" 
    width="90" 
    height="90" 
    viewBox="0 0 18 18" 
    aria-labelledby="iconspin" 
    role="presentation"
    preserveAspectRatio="xMinYMin meet"
  >
    <title id="iconspin" lang="en">icon</title>
    <g>
       <path d="M16 3H2a1 1 0 0 0-1 1v10a1 1 0 0 0 1 1h14a1 1 0 0 0 1-1V4a1 1 0 0 0-1-1zm-1.382 2L9 8.831 3.382 5h11.236zM15 12.5a.5.5 0 0 1-.5.5h-11a.5.5 0 0 1-.5-.5V7.137l5.497 3.723a.976.976 0 0 0 1.006 0L15 7.137V12.5z"/>
    </g>

  </svg>
</template>

<script>
export default {
  props: {

  },
  data(){
    return {

    }
  },
  methods:{
      hdlAnimation(){
          console.log('click!')
      }
  }
}
</script>

<style scoped>
/* svg {
  display: inline-block;
  vertical-align: baseline;
  margin-bottom: -2px;
} */
.bubble-spinner {
  display: none;
  position: absolute;
  top: -8px;
  left: -3px;
  width: 40px;
  height: 40px;
  /* margin: 100px auto; */
  background-color: #333;
  border-radius: 100%;
  -webkit-animation: sk-scaleout 1s infinite ease-in-out;
  animation: sk-scaleout 1s infinite ease-in-out;
}
.bubble-spinner-48 .bubble-spinner {
  top: -4px;
  left: -2px;
  width: 60px;
  height: 60px;
}
.bubble-spinner-36 .bubble-spinner {
  width: 65px;
  height: 65px;
  top: -14px;
  left: -7px;
}
.clicked.animate-click .bubble-spinner {
  -webkit-animation: sk-scaleout 0.3s 1 ease-in-out forwards;
  animation: sk-scaleout 0.3s 1 ease-in-out forwards;
}

.spin .bubble-spinner,
.clicked .bubble-spinner {
  display: block;
}

@-webkit-keyframes sk-scaleout {
  0% {
    -webkit-transform: scale(0);
  }
  100% {
    -webkit-transform: scale(1);
    opacity: 0;
  }
}

@keyframes sk-scaleout {
  0% {
    -webkit-transform: scale(0);
    transform: scale(0);
  }
  100% {
    -webkit-transform: scale(1);
    transform: scale(1);
    opacity: 0;
  }
}
</style>
