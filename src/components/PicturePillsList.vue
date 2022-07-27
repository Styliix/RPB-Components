<script setup>
import PicturePill from './PicturePill.vue';
import { ref, onMounted, onBeforeUnmount} from 'vue'

let isDesktop = ref(true);

defineProps({
  items: {
    type: [],
    required: true
  },
  headline : {
    type: String,
    required: true
  },
  subheadline : {
    type: String,
    required: true
  },
  link : {
    type: String,
    required: true
  },
  mobileHeadline: {
    type: String,
    required: true
  },
  mobileSubheadline : {
    type: String,
    required: true
  },
  link: {
    type: String,
    required: true
  },
  moreButtonText : {
    type: String,
    required: true
  }
});

onMounted(() => {
    resizeHandler();
    window.addEventListener('resize', resizeHandler);
});

onBeforeUnmount(() => {
    window.removeEventListener('resize', resizeHandler);
});

function resizeHandler() {
    if(window.innerWidth >= 1300) {
        isDesktop.value = true;
    }else {
        isDesktop.value = false;
    }
    console.log("isDesktop", isDesktop)
}

</script>

<template>  

    <div v-if="isDesktop">
        <a href="" class="title">{{headline}}</a>
        <p class="subtitle">{{subheadline}}</p>
        <a :href="link" class="more">{{moreButtonText}}</a>
    </div>
    <div v-if="!isDesktop">
        <a href="" class="title">{{mobileHeadline}}</a>
        <p class="subtitle">{{mobileSubheadline}}</p>
        <a :href="link" class="more">{{moreButtonText}}</a>
    </div>
    
    <div class="picturepilllist">
        <PicturePill
            v-for="pill in items"
            :title="pill.title"
            :subtitle="pill.subtitle"
            :url="pill.url"
            :imgurl="pill.imgurl"
            :twocolumns="pill.twocolumns"
        />
    </div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Quicksand:wght@500&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300&display=swap');
    .picturepilllist {
        display: flex;
        flex-wrap: wrap;
    }

    .title {
        font-size: 37px;
        text-decoration: none;
        font-weight: 600;
        color: #16828f;
        font-family: Quicksand;
    }

    .subtitle {
        font-size: 20px;
        margin-bottom: 30px;
        margin-top: -5px;
        font-family: 'Open Sans', sans-serif;
    }

    .more {
        position: absolute;
        right: 5%;
        margin-top: -85px;
        font-size: 18px;
        text-decoration: none;
        color: #16828f;
        font-weight: 600;
        font-family: 'Open Sans', sans-serif;
    }

    .abstand {
        margin-left: 10px;
    }

    @media (max-width: 1232px) {
        .picturepilllist {
            display: flex;
            flex-wrap: wrap;
        }
        .title {
            font-size: 25px;
            text-decoration: none;
            font-weight: 600;
            margin-left: 20px;
            color: #16828f;
        }

        .subtitle {
            font-size: 15px;
            margin-bottom: 20px;
            margin-top: -5px;
            margin-left: 20px;
        }  
        .more {
            position: absolute;
            right: 5%;
            margin-top: -65px;
            font-size: 14px;
            text-decoration: none;
            color: #16828f;
    }
    }

    @media (max-width: 712px) {
        .picturepilllist {
            display: block;
            flex-wrap: none;
        }
    }
</style>  