<template>
  <section class="About" id="About">
    <div class="Container">
      <div class="row">
        <div class="col col-md-3 offset-md-1">
          <Ninja />
        </div>
        <div class="col col-md-7 offset-md-1">
          <h1 class="Title">What Is</h1>
          <h3 class="Subtitle">JavaScript Conference Armenia?</h3>

          <h4 class="Answer">Where JavaScript Lovers meet!</h4>

          <p class="Description">
            JS Conf Armenia is a premier event for software engineers, hosted annually in Yerevan, Armenia. It features esteemed speakers who share their insights with JavaScript developers of varying expertise levels.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Ninja from '../_common/Ninja/Ninja.vue';

export default {
  components: {
    Ninja,
  },
};
</script>

<style scoped>
.About {
  padding-top: 50px;
  background-image: linear-gradient(to bottom, #fff, #f5f5f5);
  position: relative;
  z-index: 9;
}

.Title {
  font-size: 75px;
  text-transform: uppercase;
  color: #FF00AA;
  margin-bottom: 0;
  line-height: 1em;
}

.Subtitle {
  font-size: 28px;
  line-height: 1em;
  margin-bottom: 1em;
  text-transform: uppercase;
}

.Answer {
  font-size: 24px;
  margin-bottom: 1em;
}
</style>
