<template>
  <div class="home">
    <HeaderShayna />
    <HeroShayna />
    <WomenShayna />
    <InstaShayna />
    <LogoShayna />
    <FooterShayna />

  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import HeaderShayna from '@/components/HeaderShayna.vue'
import HeroShayna from '@/components/HeroShayna.vue'
import WomenShayna from '@/components/WomenShayna.vue'
import InstaShayna from '@/components/InstaShayna.vue'
import LogoShayna from '@/components/LogoShayna.vue'
import FooterShayna from '@/components/FooterShayna.vue'
// import carousel from 'vue-owl-carousel'

export default {
  name: 'HomeView',
  components: {
    HeaderShayna,
    HeroShayna,
    WomenShayna,
    InstaShayna,
    LogoShayna,
    FooterShayna
  }
}

</script>

