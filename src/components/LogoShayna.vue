<template>
    <!-- Partner Logo Section Begin -->
    <div class="partner-logo">
        <div class="container">
            <Carousel class="logo-carousel" :items-to-show="2.5" :wrap-around="true" :autoplay="2500">
                <Slide v-for="logo in logos" :key="logo.id">
                    <div class="logo-item">
                        <div class="tablecell-inner">
                            <img :src="logo.img" :alt="logo.img" />
                        </div>
                    </div>
                </Slide>
            </Carousel>
        </div>
    </div>
    <!-- Partner Logo Section End -->
</template>

<script>
// import { defineComponent } from 'vue'
import { Carousel, Slide } from 'vue3-carousel'
import 'vue3-carousel/dist/carousel.css'

export default {
    name: 'LogoShayna',
    components: {
        Carousel,
        Slide
    },
    data() {
        const logos = [
            {
                id: '1', img: 'img/logo-carousel/logo-1.png'
            },
            {
                id: '2', img: 'img/logo-carousel/logo-2.png'
            },
            {
                id: '3', img: 'img/logo-carousel/logo-3.png'
            },
            {
                id: '4', img: 'img/logo-carousel/logo-4.png'
            },
            {
                id: '5', img: 'img/logo-carousel/logo-5.png'
            }
        ];
        return {
            logos
        };
    }
}
</script>