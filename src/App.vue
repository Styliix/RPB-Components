<script setup>
import Quickpill from './components/QuickPill.vue';
import QuickPillListVue from './components/QuickPillList.vue';
import PicturePillsList from './components/PicturePillsList.vue';

/* TODO
* Nameing von CSS Klassen (BEM)
* Throttle von resizeHandler
* Code Formattierung
* Headline in eigene Komponente
*/

const headerProps = {
  headline: 'Desktop Headline',
  subheadLine: 'Desktop Subheadline',
  link: 'https://restplatzboerse.at',
  mobileHeadline: 'Mobile Headline',
  mobileSubheadline: 'Mobile Subheadline',
  moreButtonText: 'Mehr'
}

const items = [
  { 
    title: 'Spanien',
    subtitle: 'Spanien',
    url: '',
    imgurl: '',
    twocolumns: true
  },
  { 
    title: 'Griechenland',
    subtitle: 'Griechenland',
    url: '',
    imgurl: ''
  },
  { 
      title: 'Türkei',
      subtitle: 'Türkei',
      url: '',
      imgurl: ''
  }, 
  { 
      title: 'Italien',
      subtitle: 'Italien',
      url: '',
      imgurl: ''
  }, 
  { 
      title: 'Italien',
      subtitle: 'Italien',
      url: '',
      twocolumns: true,
      imgurl: ''
  }, 
  { 
      title: 'Italien',
      subtitle: 'Italien',
      url: '',
      imgurl: ''
  }
]
</script>

<template>
  <main>
    <div>
      <PicturePillsList
        :items="items"
        :headline="headerProps.headline"
        :subheadline="headerProps.subheadLine"
        :mobile-headline="headerProps.mobileHeadline"
        :mobile-subheadline="headerProps.mobileSubheadline"
        :more-button-text="headerProps.moreButtonText"
        :link="headerProps.link"
      />
    </div>
  </main>
</template>

<style scoped>
  div {
    margin-left: auto;
    margin-right: auto;
    max-width: 1440px;
    background-color: transparent;
  }
  @media (min-width: 1232px) {
  div {
    margin-left: auto;
    margin-right: auto;
    max-width: 1440px;
    padding-left: 60px;
    background-color: transparent;
  }
  }
</style>
