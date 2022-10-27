<template>
    <!-- Women Banner Section Begin -->
    <section class="women-banner spad">
        <div class="container-fluid">
            <div class="row">
                <div class="col-lg-12 mt-5">
                    <Carousel class="product-slider" :items-to-show="3" :wrap-around="true" :autoplay="5000">
                        <Slide v-for="slide in slides" :key="slide.id">
                            <div class="product-item">
                                <div class="pi-pic">
                                    <img :src="slide.img" :alt="slide.img" />
                                    <ul>
                                        <li class="w-icon active">
                                            <a href="#"><i class="icon_bag_alt"></i></a>
                                        </li>
                                        <router-link to="/product">
                                                <li class="quick-view">
                                                    <a href="">+ Quick View</a>
                                                </li>
                                        </router-link>
                                    </ul>
                                </div>
                                <div class="pi-text">
                                    <div class="category-name">Coat</div>
                                    <a href="#">
                                        <h5>{{ slide.product }}</h5>
                                    </a>
                                    <div class="product-price">
                                        {{ slide.price }}
                                        <span>$35.00</span>
                                    </div>
                                </div>
                            </div>
                        </Slide>

                        <template #addons>
                            <Navigation />
                            <Pagination />
                        </template>
                    </Carousel>
                </div>
            </div>
        </div>
    </section>
    <!-- Women Banner Section End -->
</template>

<script>
import { Carousel, Slide, Navigation, Pagination } from 'vue3-carousel'
import 'vue3-carousel/dist/carousel.css'

export default {
    name: 'WomenShayna',
    components: {
        Carousel,
        Slide,
        Navigation,
        Pagination
    },
    data() {
        const slides = [
            {
                id: '1', img: 'img/mickey1.jpg', product: 'Mickey Baggy', price: '$14.00'
            },
            {
                id: '2', img: 'img/products/women-2.jpg', product: 'Guangzhou sweater', price: '$13.00'
            },
            {
                id: '3', img: 'img/products/women-3.jpg', product: 'Pure Pineapple', price: '$34.00'
            },
            {
                id: '4', img: 'img/products/women-4.jpg', product: 'Converse Shoes', price: '$34.00'
            }
        ];
        return {
            slides
        };
    }
}
</script>

<style scoped>
    .product-item {
        margin-right: 25px;
    }
</style>