<template>
  <main>
    <img src="~assets/img/bg.webp" alt="" class="kv">
    <img src="~assets/img/headings.png" alt="" class="headings">

    <div class="buttons">
      <img src="~assets/img/buy.png" alt="" class="button-play" id="Button1">
      <img src="~assets/img/sell.png" alt="" class="button-play" id="Button2">
      <img src="~assets/img/rent.png" alt="" class="button-play" id="Button3">
      <img src="~assets/img/know.png" alt="" class="button-play" id="Button4">
      <img src="~assets/img/contact.png" alt="" class="button-play" id="Button5">
    </div>
    
    <div class="news">
      <h5>ニュース・イベント</h5>
      <img src="~assets/img/info.png" alt="">
    </div>

  </main>
</template>

<script>
export default {
  name: 'IndexPage',
  mounted () {

    
    const target1 = document.getElementById('Button1')
    const target2 = document.getElementById('Button2')
    const target3 = document.getElementById('Button3')
    const target4 = document.getElementById('Button4')
    const target5 = document.getElementById('Button5')

    target5.addEventListener('animationend', () => {
      target1.classList.remove("button-play")
      setInterval(
        function(){
          target1.classList.add("button-play")},0)
    })

    target5.addEventListener('animationend', () => {
      target2.classList.remove("button-play")
      setInterval(
        function(){
          target2.classList.add("button-play")}, 0)
    })

    target5.addEventListener('animationend', () => {
      target3.classList.remove("button-play")
      setInterval(
        function(){
          target3.classList.add("button-play")}, 0)
    })

    target5.addEventListener('animationend', () => {
      target4.classList.remove("button-play")
      setInterval(
        function(){
          target4.classList.add("button-play")}, 0)
    })

    target5.addEventListener('animationend', () => {
      target5.classList.remove("button-play")
      setInterval(
        function(){
          target5.classList.add("button-play")}, 0)
    })


  },
}

</script>

<style>
  
main {
  width: 100vw;
  height: 100vh;
  position: relative;
  padding: 0 12.5vw;
}
.headings {
  position: absolute;
  top: 50%;
  left: auto;
  transform: translateY(-50%);
  height: 13rem;
}

.buttons {
  position: absolute;
  top: auto;
  bottom: 3rem;
  width: 50rem;
  display: flex;
  flex-wrap: wrap;
}
.buttons img {
  height: 4.5rem;
  margin-right: 3rem;
  margin-bottom: 2rem;
}

.news {
  position: absolute;
  top: auto;
  bottom: 4rem;
  left: auto;
  right: 10vw;
}
.news h5 {
  position: relative;
  font-size: 1.73rem;
  color: white;
}
.news img {
  margin-top: 2.5rem;
  height: 5.75rem;}

.news h5::after {
  content: "";
  width: 15.5rem; 
  height: 1px; 
  position: absolute; 
  bottom: -.25rem; 
  left: 0;
  margin: 0 auto; 
  overflow: hidden; 
  background: linear-gradient(to right, white 50%, rgba(255, 255, 255, 0) 50%); 
  background-position: -15.5rem 0; 
  background-size: 200% 100%; 
  animation: animation 5s cubic-bezier(0.85, 0, 0.3, 1) forwards infinite;
}

@keyframes animation {
  0% { background-position: -15.5rem 0; }
  45% { background-position: 0 0; }
  90% { background-position: 15.5rem 0; }
  100% { background-position: 15.5rem 0; }
}

.buttons img {opacity: .5;}
.buttons .button-play:nth-of-type(1) {animation: button1 4s 0s alternate forwards;}
.buttons .button-play:nth-of-type(2) {animation: button1 4s 3s alternate forwards;}
.buttons .button-play:nth-of-type(3) {animation: button1 4s 6s alternate forwards;}
.buttons .button-play:nth-of-type(4) {animation: button1 4s 9s alternate forwards;}
.buttons .button-play:nth-of-type(5) {animation: button1 4s 12s alternate forwards;}
@keyframes button1 {
  0% { opacity: 0.5 }
  50% { opacity: 1 }
  100% { opacity: 0.5 }
}
/*
@keyframes button2 {
  25% { opacity: 0.5 }
  50% { opacity: 1 }
  75% { opacity: 0.5 }
}

@keyframes button3 {
  37.5% { opacity: 0.5 }
  50% { opacity: 1 }
  62.5% { opacity: 0.5 }
}

@keyframes button4 {
  43.75% { opacity: 0.5 }
  50% { opacity: 1 }
  56.25% { opacity: 0.5 }
}

@keyframes button5 {
  46.875% { opacity: 0.5 }
  50% { opacity: 1 }
  53.125% { opacity: 0.5 }
}
*/



.kv {
  margin-left: -12.5vw;
  width: 100vw;
  height: 100vh;
}


</style>
