<script setup>
defineProps({
  msg: {
    type: String,
    required: true
  },
  url: {
    type: String,
    required: true
  },
  imgurl: {
    type: String,
    required: true
  }
})
</script>

<template>
    <div class="wrapper">
      <a href="">
        <div class="div">
          <span>Reiseziele August</span>
        </div>
      </a>
    </div>
</template>

<style scoped>

  .wrapper {
    background-color: green;
    width: 405px;
    height: 235px;
    border-radius: 20px;
    margin: 0 auto;
    float: left;
    background-image: url('src/assets/img/Paradiesischer-Urlaub.jpg');
    background-size: cover;
  }

  a {
    text-decoration: none;
  }

  .div {
    background-color: rgb(1, 1, 1, 0.4);
    width: 405px;
    height: 235px;
    border-radius: 20px;
  }

  span {
    width: 500px;
    height: 50px;
    background-color: rgb(3, 194, 149);
    padding-left: 50px;
    padding-right: 50px;
    padding-top: 15px;
    padding-bottom: 15px;
    border-radius: 30px;
    font-size: 20px;
    color: white;
    margin-left: 70px;
    top: 105px;
  }

   @media (max-width: 1900px) {
    .wrapper {
    background-color: black;
    width: 355px;
    height: 215px;
    border-radius: 20px;
    margin-top: 15px;
    margin-left: auto;
    margin-right: auto;
    float: none;
  }

  .div {
    background-color: rgb(1, 1, 1, 0.4);
    width: 355px;
    height: 215px;
    border-radius: 20px;
  }

  span {
    width: 500px;
    height: 50px;
    background-color: rgb(3, 194, 149);
    padding-left: 40px;
    padding-right: 40px;
    padding-top: 12px;
    padding-bottom: 12px;
    border-radius: 30px;
    font-size: 20px;
    color: white;
    margin-left: 60px;
    top: 98px;
  }

   }

  @media (max-width: 819px) {
  .wrapper {
    background-color: black;
    width: 305px;
    height: 175px;
    border-radius: 20px;
    margin-top: 15px;
    margin-left: auto;
    margin-right: auto;
    float: none;
  }

  .div {
    background-color: rgb(1, 1, 1, 0.4);
    width: 305px;
    height: 175px;
    border-radius: 20px;
  }

  span {
    background-color: rgb(3, 194, 149);
    padding-left: 30px;
    padding-right: 30px;
    padding-top: 10px;
    padding-bottom: 10px;
    border-radius: 30px;
    font-size: 18px;
    color: white;
    margin-left: 55px;
    top: 80px;
  }

  }

</style>