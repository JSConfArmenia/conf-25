<template>
  <section class="Intro" id="Intro">
    <div class="Container">
      <h1 class="Title">JavaScript Conference <br> Armenia</h1>
      <h2 class="Subtitle">Armenak Armenakyan 4, Yerevan</h2>
      <h3 class="Subtitle">June 9, 2024</h3>
      <a href="https://fienta.com/js-conf-armenia-2024" class="Button -call-to-action" target="_blank">
        Get your ticket!
      </a>
    </div>

    <div class="IntroSponsor">
      <div class="Description">
        General sponsors
      </div>
      <div class="sponsor-logos-container">
        <div>
          <a href="https://rewards.adobe.com/armenia/" target="_blank">
            <img class="IntroSponsorAdobe" src="/sponsors/adobe-bw.svg" /> 
          </a>
        </div>
        <div>
          <a href="https://www.simplytechnologies.net/" target="_blank">
            <img src="/sponsors/simply-bw.svg" />
          </a>
        </div>
      </div>
    </div>

    <div class="IntroBgLeft"></div>
    <!-- <div class="IntroBgMain"></div> -->
    <!-- <div class="IntroBgRight"></div> -->
  </section>
</template>

<script>
export default {

};
</script>

<style scoped lang="scss">
.Intro {
  min-height: 100vh;
  display: flex;
  padding: 150px 0;
  align-items: center;
  justify-content: flex-start;
}

.Title {
  font-size: 60px;
  line-height: 70px;
  font-weight: 900;
  text-transform: none;
}

.Subtitle {
  font-size: 36px;
}

.IntroSponsor {
  position: absolute;
  right: 5%;
  bottom: 50px;
  display: block;
  font-size: .8em;
  text-align: center;
  width: 200px;
}

.IntroSponsor img {
  margin: 16px 0;
}

.IntroSponsorAdobe {
  width: 150px;
}

.IntroBgLeft {
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-image: url('./IntroBgLeft.svg');
  background-repeat: no-repeat;
  background-size: contain;
  z-index: -1;
}

.IntroBgMain {
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-image: url('./IntroBgMain.png');
  background-repeat: no-repeat;
  background-size: 60vh;
  background-position-y: 65%;
  background-position-x: center;
  z-index: -1;
}

.IntroBgRight {
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  z-index: -1;

  &:after {
    position: absolute;
    left: 65%;
    top: 15%;
    width: 30vh;
    height: 30vh;
    border-radius: 50%;
    background-color: #ffdd00;
    display: block;
    content: " ";
  }
}

@media (max-width: 450px) {
  .sponsor-logos-container {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
  }

  .Subtitle {
    text-shadow: 1px 1px 1px black;
    font-size: 16px;
  }

  .IntroBgMain {
    opacity: 0.77;
  }
}

@media (max-width: 700px) {
  .IntroBgRight {
    &:after {
      height: 25vw;
      left: 75%;
      top: 17%;
      width: 25vw;
    }
  }

  .Title {
    font-size: 48px;
  }

  .Subtitle {
    font-size: 18px;
  }

  .IntroSponsor {
    right: initial;
    bottom: 5px;
    display: flex;
    flex-direction: column;
    width: 100%;
  }
}

@media (max-width: 600px) {
  .Button {
    padding: 0.7em 2em;
  }

  .IntroSponsor img {
    width: 100px;
    margin: 10px;
  }

  .Title {
    line-height: 55px;
  }

  .Subtitle {
    font-size: 27px;
  }

  .IntroBgMain,
  .IntroBgRight {
    top: -20px;
  }
}

@media (max-height: 550px) {
  .Container {
    margin: -45px auto;
  }

  .Title {
    line-height: 55px;
    font-size: 40px;
  }
}

</style>
