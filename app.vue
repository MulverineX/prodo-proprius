<template>
  <div id="main">
    
    <div id="space">
      <div class="stars"></div>
      <div class="stars"></div>
      <div class="stars"></div>
      <div class="stars"></div>
      <div class="stars"></div>
    </div>
    <div id="space">
      <div class="stars"></div>
      <div class="stars"></div>
      <div class="stars"></div>
      <div class="stars"></div>
      <div class="stars"></div>
    </div>
    <div id="content">
      <center><div id="header">
        <h1>Prodo Proprius</h1>
      </div></center>
    </div>
  </div>
</template>

<style lang="less">
@import url('https://fonts.googleapis.com/css2?family=Rajdhani:wght@700&display=swap');
/* Stars 
------------------------------------- */

#space, .stars {
  overflow: hidden;
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
}

.stars {
  background-image: 
    radial-gradient(20px 20px at 20px 30px, rgba(0, 114, 140, 1), rgba(0, 114, 140,.1)),
    radial-gradient(20px 20px at 40px 70px, rgba(11, 100, 151, 1), rgba(11, 100, 151,.1)),
    //radial-gradient(20px 20px at 50px 160px, #214B8F, rgba(0,0,0,0)),
    radial-gradient(20px 20px at 90px 40px, rgba(79, 64, 133, 1), rgba(79, 64, 133,.1)),
    radial-gradient(20px 20px at 130px 80px, rgba(153, 62, 101, 1), rgba(153, 62, 101,.1));
    //radial-gradient(20px 20px at 160px 120px, #993E65, rgba(0,0,0,0));
  background-repeat: repeat;
  background-size: 150px 150px;
  animation: zoom 10s infinite;
  opacity: 0;
}

.stars:nth-child(1) {
  background-position: 50% 50%;
  animation-delay: 0s;
}
.stars:nth-child(2) {
  background-position: 20% 60%;
  animation-delay: 1s;
}
.stars:nth-child(3) {
  background-position: -20% -30%;
  animation-delay: 2s;
}
.stars:nth-child(4) {
  background-position: 40% -80%;
  animation-delay: 4s;
}
.stars:nth-child(5) {
  background-position: -20% 30%;
  animation-delay: 8s;
}

@keyframes zoom {
  0% {
    opacity: 0;
    transform: scale(0.5);
    animation-timing-function: ease-in;
  } 
  85% {
    opacity: 1;
    transform: scale(2.8);
    animation-timing-function: linear;
  }
  100% {
    opacity: 0;
    transform: scale(3.5);
  }
}

/* Demo syles 
------------------------------------- */
body {
  background: #000;
  width: max-content;
  height: max-content;
  margin: 0;
}

#content {
  position: absolute;
  z-index: 1000;
  background: rgba(0,0,0,0.4);
  width: 100%;
  height: 100%;
  backdrop-filter: blur(30px);

  #header {
    margin: 2rem;

    justify-self: center;
    display: flex;

    height: 5rem;
    background-color: rgba(0,0,0,0.4);
    border-radius: 1rem;

    h1 {
      margin-left: 2rem;
      
      font-family: 'Rajdhani';
      color: rgba(11, 100, 151, 1);
      text-justify: center;
    }
  }
}
</style>