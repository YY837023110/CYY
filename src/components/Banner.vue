<template>
    <div class="swiper-container">
        <div class="swiper-wrapper">
            <div class="swiper-slide" v-for="(item,index) in listImgs" :key="index">
                <img :src="item.url" alt="">
            </div>
        </div>
        <div class="swiper-pagination swiper-pagination-white"></div>
    </div>
</template>

<script>
    import Swiper from 'swiper';
    import '../../static/css/swiper.min.css';
    export default {
        
        props: ['listImgs'],
        mounted() {
            console.log('mounted', this);
            console.log(this.listImgs)
            var swiper = new Swiper('.swiper-container', {
                pagination: '.swiper-pagination',
                paginationClickable: true,
                loop: true,
                speed: 600,
                autoplay: 4000,
                onTouchEnd: function() {
                    swiper.startAutoplay()
                }
            });
        }
    }
</script>