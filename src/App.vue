<script setup>
import { ref, onMounted } from 'vue'

const isMobile = ref(false)

onMounted(() => {
  // Check if device is mobile based on screen width and user agent
  const checkMobile = () => {
    const width = window.innerWidth
    const userAgent = navigator.userAgent.toLowerCase()
    const mobileKeywords = ['mobile', 'android', 'iphone', 'ipad', 'tablet']

    return width <= 768 || mobileKeywords.some(keyword => userAgent.includes(keyword))
  }

  isMobile.value = checkMobile()

  // Listen for window resize to handle orientation changes
  window.addEventListener('resize', () => {
    isMobile.value = checkMobile()
  })
})
</script>

<template>
  <!-- Desktop Only Message -->
  <div v-if="!isMobile" class="desktop-only-container">
    <div class="desktop-message">
      <h1 class="desktop-title">📱 Oops! This invitation is mobile-exclusive! 📱</h1>
      <div class="phone-emoji">📱</div>
      <p class="desktop-text">
        This magical wedding invitation was crafted specifically for your phone!
        <br><br>
        🎭 <em>Please grab your mobile device and open this link there for the full enchanting experience!</em>
        <br><br>
        Trust us, it's worth the extra step! ✨
      </p>
      <div class="hearts">💕 💍 💕</div>
    </div>
  </div>

  <!-- Mobile Content -->
  <div v-else>
    <div style="position: relative; margin-bottom: 47px;">
      <img src="./assets/images/main-image.svg" alt="main image" class="main-image" width="100%" />
      <h1 class="title">Ghina <span style="font-family: Dosis; font-weight: 400;">&</span> Maytham</h1>
      <h3 class="subtitle">We<span style="font-family: sans-serif">'</span>re getting engaged<span
          style="font-family: Andada Pro ;">!</span></h3>
    </div>
    <h3 class="join-us">Join us for a celebration of love<span style="font-family: Adamina;">,</span> laughter<span
        style="font-family: Adamina;">,</span> and the
      start of forever <span class="heart-style">b</span></h3>

    <div>
      <h1 class="title2" style="color: black;">In the Little Things</h1>
    </div>
    <div class="container1">

      <img src="./assets/images/PRINT.svg" alt="print image" class="print-img" />
      <img src="./assets/images/coffee.svg" alt="heart image" class="coffee-img" />
      <img src="./assets/images/beach.svg" alt="heart image" class="beach-img" />
      <!-- <img src="./assets/images/story.jpg" class="story-img" /> -->
      <p class="story-text">From coffee dates to quiet sunsets<span style="font-family: Adamina;">,</span> our love grew
        in the little moments <span class="small-heart">I</span></p>
    </div>
    <div
      style="display: flex;flex-direction: column;justify-content: center;align-items: center;position: relative;margin-bottom: 50px;">
      <img src="./assets/images/PRINT2.svg" alt="heart image" class="print2" />
      <h1 class="title2">Date <span style="text-transform: lowercase;">and</span> Place</h1>
      <img src="./assets/images/cal.svg" class="Calender" style="width: 95%;" />

    </div>

    <div class="timeContainer">
      <h1 class="time">Hit the map and we<span style="font-family: sans-serif">'</span>ll see you there <span
          style="text-transform: lowercase;">at</span> <span style="font-family: El Messiri;">8:00</span> PM</h1>
      <a href="https://maps.app.goo.gl/1spxXDfXs6Ua9RMc9?g_st=ic"><img src="./assets/images/maps.svg"
          class="maps-img" /></a>
    </div>

    <div class="dressContainer">
      <img src="./assets/images/dress.svg" class="dress-img" />
      <h1 class="title2">Dress the Vibe</h1>
    </div>
    <p class="textt">Ladies<span style="font-family: Adamina;">,</span> think pastels<span
        style="font-family: Adamina;">,</span> creams<span style="font-family: Adamina;">,</span> florals<span
        style="font-family: Adamina;">,</span> and flowy things<span style="font-family: Adamina;">.</span></p>
    <p class="textt">And Gentlemen… black<span style="font-family: Adamina;">.</span> Just black<span
        style="font-family: Adamina;">.</span> You<span style="font-family: sans-serif">'</span><span
        style="text-transform: lowercase;">re</span> welcome<span style="font-family: Andada Pro ;">!</span><img
        src="./assets/images/shirt.svg" class="heartz" /></p>

    <div style="position: relative;margin-top: 50px;">
      <img src="./assets/images/us.svg" width="100%" />
      <div class="footer-text">
        <h3 class="footer-t" style="color: white;">Come for the love<span style="font-family: Adamina;">,</span> stay
          for
          the party<span style="font-family: Andada Pro ;">!</span> We can<span
            style="font-family: sans-serif">'</span><span style="text-transform: lowercase;">t</span> wait to dance<span
            style="font-family: Adamina;">,</span>
          laugh<span style="font-family: Adamina;">,</span> and celebrate with you <span class="heart-style">b</span>
        </h3>

      </div>
    </div>
  </div>
</template>

<style scoped>
/* Desktop Only Styles */
.desktop-only-container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background: linear-gradient(135deg, #ff9a9e 0%, #fecfef 50%, #fecfef 100%);
  padding: 20px;
}

.dress-img {
  position: absolute;
  left: 40px;

}

.story-text {
  color: #1F1F1F;

  font-family: "Orliet Pro";
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  width: 175px;
  height: 72px;
  position: absolute;
  top: 12%;
  right: 30px;

}

.small-heart {
  color: #1F1F1F;
  font-family: BonusHearts;
  font-size: 16px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
}

.desktop-message {
  background: white;
  padding: 60px 40px;
  border-radius: 20px;
  text-align: center;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
  max-width: 600px;
  width: 100%;
  animation: bounce 2s ease-in-out infinite;
}

.desktop-title {
  color: #B700FF;
  font-size: 2.5rem;
  margin-bottom: 20px;
  font-weight: bold;
  line-height: 1.2;
}

.phone-emoji {
  font-size: 4rem;
  margin: 20px 0;
  animation: wiggle 1s ease-in-out infinite;
}

.desktop-text {
  font-size: 1.2rem;
  color: #333;
  line-height: 1.6;
  margin: 30px 0;
}

.hearts {
  font-size: 2rem;
  margin-top: 30px;
  opacity: 0.8;
}

@keyframes bounce {

  0%,
  20%,
  50%,
  80%,
  100% {
    transform: translateY(0);
  }

  40% {
    transform: translateY(-10px);
  }

  60% {
    transform: translateY(-5px);
  }
}

@keyframes wiggle {

  0%,
  100% {
    transform: rotate(0deg);
  }

  25% {
    transform: rotate(-10deg);
  }

  75% {
    transform: rotate(10deg);
  }
}

/* Original Mobile Styles */
.comeForThe {
  font-family: 'Orliet Pro';
}

.heart-style {
  color: #B700FF;
  font-family: Heartz;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  text-transform: uppercase;
}

.print2 {
  position: absolute;
  top: 20px;
  left: 0;
  z-index: -1;
  height: auto;
}

.span {
  font-family: Adamina;
}

.comeForTheLoveStayForTh {
  text-transform: capitalize;
}

.b {
  text-transform: uppercase;
  font-family: Heartz;
  color: #b700ff;
}

.comeForTheContainer {
  width: 329px;
  position: relative;
  font-size: 16px;
  text-align: center;
  display: inline-block;
  color: #fff;
  font-family: 'Orliet Pro';
}

.container1 {
  position: relative;
  width: 100%;
  height: auto;
  min-height: 350px;
  margin-bottom: 20px;
  margin-bottom: 52px;
}

.footer-text {
  position: absolute;
  bottom: 30px;
  left: 50%;
  transform: translateX(-50%);
  width: 100%;
}

.footer-t {
  color: #FFF;

  text-align: center;
  font-family: "Orliet Pro";
  font-size: 16px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;
  text-transform: capitalize;
  text-align: center;
  margin: 0 20px;
}

.textt {
  color: #1F1F1F;
  width: 100%;
  text-align: center;
  font-family: "Orliet Pro";
  font-size: 16px;
  letter-spacing: -0.32px;
  font-style: normal;
  font-weight: 400;
  line-height: 0px;
  text-transform: capitalize;
}

.dressContainer {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 65px;
  /* margin-bottom: 20px; */
}

.dressContainer h1 {
  width: 50%;
}

.Calender {
  margin-top: 25px;
}

.timeContainer {
  position: relative;
}

.maps-img {
  position: absolute;
  top: -60%;
  /* left: 50%; */
  /* transform: translate(-50%, -50%); */
  right: 30px;
  height: auto;
}

.time {
  color: #000;
  max-width: 160px;
  font-family: "Orliet Pro";
  margin-left: 35px;
  font-size: 20px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  text-transform: uppercase;
}

.print-img {
  position: absolute;
  top: 0;
  right: 0;
  height: auto;
}

.story-img {
  position: absolute;
  top: 18%;
  right: 45px;
  height: auto;
}

.beach-img {
  position: absolute;
  bottom: 0;
  right: 0;
  height: auto;
}

.coffee-img {
  position: absolute;
  top: 30px;
  left: 0;
  height: auto;
}

.heartz {
  vertical-align: middle;
  /* Aligns it vertically with text */
  /* height: 1em; */
  /* Makes the image roughly the size of the text */
  display: inline-block;
  /* Ensures it's treated as inline content */
  margin-left: 5px;
  /* Adds a small space before the heart */
}

.title {
  position: absolute;
  top: 13px;
  left: 50%;
  font-family: "Orliet Pro";
  transform: translateX(-50%);
  font-size: 36px;
  /* font-family: "Orliet Pro"; */
  color: white;
  width: 100%;
  text-align: center;
  text-transform: uppercase;
}

.title2 {
  color: #000;

  font-family: "Orliet Pro";
  font-size: 24px;
  font-style: normal;
  font-weight: 700;
  /* line-height: 0; */
  text-transform: uppercase;
  width: 100%;
  text-align: center;
}

.subtitle {
  color: #FFF;
  font-family: "Orliet Pro";
  font-size: 20px;
  font-style: normal;
  font-weight: 400;
  line-height: 0;
  text-transform: uppercase;
  position: absolute;
  bottom: 20px;
  left: 50%;
  transform: translateX(-50%);
  width: 100%;
  text-align: center;
}

.join-us {
  color: #1F1F1F;
  margin: 0px 47px;
  text-align: center;
  font-family: "Orliet Pro";
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  text-transform: capitalize;
  align-items: center;
  margin-bottom: 47px;
}
</style>