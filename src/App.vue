<script setup>

</script>

<template>
  <div style="position: relative; margin-bottom: 51px;">
    <img src="./assets/images/main-image.svg" alt="main image" class="main-image" width="100%" />
    <h1 class="title">Ghina <span style="font-family: Dosis; font-weight: 400;">&</span> Maytham</h1>
    <h3 class="subtitle">We’re getting engaged<span style="font-family: Andada Pro ;">!</span></h3>
  </div>
  <h3 class="join-us">Join us for a celebration of love<span style="font-family: Adamina;">,</span> laughter<span
      style="font-family: Adamina;">,</span> and the
    start of forever <span class="heart-style">b</span></h3>

  <h1 class="title2" style="color: black;">In the Little Things</h1>
  <div class="container1">
    <img src="./assets/images/PRINT.svg" alt="print image" class="print-img" />
    <img src="./assets/images/coffee.svg" alt="heart image" class="coffee-img" />
    <img src="./assets/images/beach.svg" alt="heart image" class="beach-img" />
    <img src="./assets/images/story.jpg" class="story-img" />
  </div>
  <div style="display: flex;flex-direction: column;justify-content: center;align-items: center;position: relative;">
    <img src="./assets/images/PRINT2.svg" alt="heart image" class="print2" />
    <h1 class="title2">Date <span style="text-transform: lowercase;">and</span> Place</h1>
    <img src="./assets/images/calendar.svg" class="Calender" style="width: 95%;" />

  </div>

  <div class="timeContainer">
    <h1 class="time">Hit the map and we’ll see you there <span style="text-transform: lowercase;">at</span> <span
        style="font-family: El Messiri;">8:00</span> PM</h1>
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
  <p class="textt">And Gentlemen… black. Just black. You're welcome<span style="font-family: Andada Pro ;">!</span><img
      src="./assets/images/shirt.svg" class="heartz" /></p>

  <div style="position: relative;margin-top: 50px;">
    <img src="./assets/images/us.svg" width="100%" />
    <div class="footer-text">
      <h3 class="footer-t" style="color: white;">Come for the love<span style="font-family: Adamina;">,</span> stay for
        the party<span style="font-family: Andada Pro ;">!</span> We can’t wait to dance<span
          style="font-family: Adamina;">,</span>
        laugh<span style="font-family: Adamina;">,</span> and celebrate with you <span class="heart-style">b</span></h3>

    </div>
  </div>
</template>

<style scoped>
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
  margin: 0 30px;
}

.textt {
  color: #1F1F1F;
  width: 100%;
  text-align: center;
  font-family: "Orliet Pro";
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  text-transform: capitalize;
}

.dressContainer {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 50px;
  margin-bottom: 20px;
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
  top: -50%;
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
  top: 34px;
  left: 50%;
  font-family: "Orliet Pro";
  transform: translateX(-50%);
  font-size: 36px;
  /* font-family: "Orliet Pro"; */
  color: white;
  width: 100%;
  text-align: center;
}

.title2 {
  color: #000;

  font-family: "Orliet Pro";
  font-size: 24px;
  font-style: normal;
  font-weight: 700;
  line-height: 0;
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
  line-height: normal;
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
  font-weight: 700;
  line-height: normal;
  text-transform: capitalize;
  align-items: center;
  margin-bottom: 47px;
}
</style>
