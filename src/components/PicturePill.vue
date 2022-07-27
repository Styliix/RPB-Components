<script setup>
defineProps({
  title: {
    type: String,
    required: true
  },
  subtitle: {
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
  },
  twocolumns: {
    type: Boolean,
    required: false
  }

})
</script>

<template>
    <div class="picturepilldiv" :class="{'twocolumn' : twocolumns}">
        <a href="">
            <div class="picturepill">
                <div class="titles">
                  <h1 class="title">{{title}}</h1>
                  <span class="subtitlespan">{{subtitle}}</span>
                </div>
            </div>
        </a>
    </div>
</template>

<style scoped>

@import url('https://fonts.googleapis.com/css2?family=Quicksand:wght@500&display=swap');

.picturepilldiv {
    font-family: Quicksand;
    width: 22.5%;
    height: 400px;
    background-image: url('src/assets/img/Paradiesischer-Urlaub.jpg');
    background-size: cover;
    margin-left: 0.48%;
    margin-right: 10px;
}

.picturepill {
    width: 100%;
    height: 400px;
    background-color: rgb(1, 1, 1, 0.1);
    transition: .5s;
}

.picturepill:hover {
    box-shadow: 0rem 0.2rem 0.8rem rgb(0 0 0 / 40%);
}

.twocolumn {
    width: 46.2%;
    height: 400px;
    background-image: url('src/assets/img/Paradiesischer-Urlaub.jpg');
    background-size: cover;
    margin-bottom: 20px;
}

.titles {
    position: absolute;
    width: 100%;
    bottom: 0px;
    background-color: rgba(255, 255, 255, 0.9);
    text-align: center;
    padding-top: 15px;
    padding-bottom: 15px;
    padding-left: 5px;
    padding-right: 5px;
}

.title {
  font-size: 30px;
  color: black;
}

.subtitlespan{
  font-size: 20px;
  color: black;
}

@media (max-width: 1232px) {
  .picturepilldiv {
    width: 45.1667%;
    height: 400px;
    background-image: url('src/assets/img/Paradiesischer-Urlaub.jpg');
    background-size: cover;
    margin-left: auto;
    margin-bottom: 20px;
    margin-right: auto;
  }
}

@media (max-width: 712px) {
      .picturepilldiv {
        margin-left: auto;
        margin-right: auto;
        margin-top: 15px;
        width: 90.1667%;
        height: 500px;
      }

      .picturepill {
        width: 100%;
        height: 500px;
        background-color: rgb(1, 1, 1, 0.1);
      }

      .titles {
        position: absolute;
        width: 100%;
        bottom: 0px;
        background-color: rgba(255, 255, 255, 0.9);
      } 

}

</style>