<template>
  <div class="Location" id="Location">
    <h2 class="Title">Location</h2>

    <div class="MapContainer">
      <div class="smart-object"></div>
      <iframe
        class="Map"
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d333.71691723874!2d44.53161966594959!3d40.19004225802676!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x406abdf02990f5b3%3A0x61e1f8b7191b33a0!2sSynergy%20Business%20Center%202nd%20building!5e0!3m2!1sen!2sam!4v1714049521675!5m2!1sen!2sam" width="800" height="600" frameborder="0" style="border:0" allowfullscreen>
      </iframe>

      <span class="text">HERE WE ARE!</span>
    </div>
  </div>
</template>

<script>
export default {

};
</script>

<style scoped lang="scss">
.Location {
  padding: 50px 0 100px 0;
  position: relative;
}

.Title {
  text-align: center;
  color: #FF00AA;
  margin-bottom: 30px;
}

.MapContainer {
  display: flex;
  align-items: center;
  justify-content: space-evenly;
}

.smart-object {
  background-image: url('./smartObject.png');
  width: 130px;
  height: 200px;
  background-repeat: no-repeat;
}

.text {
  color: black;
  // font-weight: bold;
  font-size: 30px;
  text-align: center;
}

.Map {
  width: 50vw;
  height: 30vw;
  top: 0;
  left: 0;
  box-shadow: 1px -4px 23px -6px grey;
  border-radius: 10px;
  overflow: hidden;
}

@media (max-width: 680px) {
  .Location {
    flex-direction: column;
    padding: 50px 0;
  }

  .smart-object {
    display: none;
  }

  .text {
    display: block;
    margin-top: 15px;
    font-size: 25px;
  }

  .Map {
    width: 100%;
    height: 50vw;
  }
}

</style>
