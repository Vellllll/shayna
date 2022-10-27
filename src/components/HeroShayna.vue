<template>
    <Carousel>
        <Slide v-for="slide in slides" :key="slide.id">
            <div class="single-hero-items set-bg" :style="{'background-image': `url(${slide.gambar})`}">
                <div class="container">
                    <div class="row">
                        <div class="col-lg-5">
                            <span>Bag,kids</span>
                            <h1>Black friday</h1>
                            <p>
                                Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore
                            </p>
                            <a href="#" class="primary-btn">Shop Now</a>
                        </div>
                    </div>
                </div>
            </div>
        </Slide>

        <template #addons>
            <Navigation />
            <Pagination />
        </template>
    </Carousel>

</template>

<script>
import { Carousel, Slide, Navigation, Pagination } from 'vue3-carousel'
import 'vue3-carousel/dist/carousel.css'
export default {
    name: 'HeroShayna',
    components: {
        Carousel,
        Slide,
        Navigation,
        Pagination
    },
    data() {
        const slides = [
            {
                id:'1', gambar: '/img/hero-1.jpg'
            },
            {
                id:'2', gambar: '/img/hero-2.jpg'
            }
        ];
        return {
            slides,
        };
    }
}
</script>