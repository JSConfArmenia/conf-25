<template>
  <div class="Location" id="Location">
    <h2 class="Title">Location</h2>

    <div class="MapContainer">
      <div class="smart-object"></div>
      <iframe
        class="Map"
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3047.855609274551!2d44.531557899999996!3d40.1900267!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x406abcdbd90d7789%3A0xcf0375615284b006!2s5%2C%202%20Armenak%20Armenakyan%20St%2C%20Yerevan!5e0!3m2!1sen!2sam!4v1759317896448!5m2!1sen!2sam" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
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
