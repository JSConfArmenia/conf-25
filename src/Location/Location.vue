<template>
  <div class="Location" id="Location">
    <h2 class="Title">Location</h2>

    <div class="MapContainer">
      <div class="smart-object"></div>

      <iframe
        class="Map"
        src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d12194.405990222456!2d44.5073634!3d40.1734255!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x6ca36012e8fad5e!2sSundukyan%20State%20Academic%20Theatre!5e0!3m2!1sen!2s!4v1623867541385!5m2!1sen!2s" width="800" height="600" frameborder="0" style="border:0" allowfullscreen>
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
  color: #198dbf;
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
  color: #757575;
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
    margin-bottom: 15px;
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
