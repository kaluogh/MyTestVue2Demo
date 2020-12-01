
<template>
    <main class="page">
        <header class="header">
            <img src="../assets/chinamobile.png" alt="logo">
        </header>

        <section class="banner">
            <swiper
                class="swiper"
                :options="swiperOption"
                @swiper="onSwiper"
                @slideChange="onSlideChange"
            >
                <swiper-slide>
                    <div class="slide-container">
                        <img src="../assets/banner1.png" />
                    </div>
                </swiper-slide>
                <swiper-slide>
                    <div class="slide-container">
                        <img src="../assets/banner2.png" />
                    </div>
                </swiper-slide>
                <swiper-slide>
                    <div class="slide-container">
                        <img src="../assets/banner3.png" />
                    </div>
                </swiper-slide>
                <swiper-slide>
                    <div class="slide-container">
                        <img src="../assets/banner4.png" />
                    </div>
                </swiper-slide>
                <swiper-slide>
                    <div class="slide-container">
                        <img src="../assets/banner5.png" />
                    </div>
                </swiper-slide>

                <!-- Optional controls -->
                <!-- <div class="swiper-pagination" slot="pagination"></div> -->
                <div class="swiper-button-prev" slot="button-prev"></div>
                <div class="swiper-button-next" slot="button-next"></div>

            </swiper>
        </section>

        <section class="list">
            <div class="more more-item1">
                <div class="title">
                    <img src="../assets/title1.png" alt="">
                </div>
                <div class="content">
                    <b>15GB专属流量 + 爱奇艺会员</b>
                    <p>好剧放心看，组合更优惠，立省12.1元/月</p>
                    <div>
                        <span>原价28</span>
                        <button>立即办理</button>
                    </div>
                    <div>
                        <span>15.9</span>
                        <span>前3个月</span>
                        <img src="../assets/pay.png" alt="">
                    </div>
                </div>
            </div>
            <div class="divider">
                <img src="../assets/divider.png" alt="">
            </div>
            <div class="more more-item2">
                <div class="content">
                    <b>15GB专属流量 + 爱奇艺会员</b>
                    <p>好剧放心看，组合更优惠，立省12.1元/月</p>
                    <div>
                        <span>原价28</span>
                        <button>立即办理</button>
                    </div>
                    <div>
                        <span>15.9</span>
                        <span>前3个月</span>
                        <img src="../assets/pay.png" alt="">
                    </div>
                </div>
            </div>
        </section>
    </main>
</template>

<script>
import { swiper, swiperSlide } from 'vue-awesome-swiper'
import 'swiper/swiper-bundle.css'

export default {
    name: 'Ad',
    data() {
        return {
            swiperOption: {
                loop: true,
                autoplay: {
                    delay: 3000,
                    stopOnLastSlide: false,
                    disableOnInteraction: false
                },
                // 显示分页
                // pagination: {
                //     el: ".swiper-pagination",
                //     clickable: true //允许分页点击跳转
                // },
                // 设置点击箭头
                navigation: {
                    prevEl: ".swiper-button-prev",
                    nextEl: ".swiper-button-next",
                }
            }
        };
    },
    components: {
        swiper,
        swiperSlide,
    },
    methods: {
        onSwiper(swiper) {
            console.log(swiper)
        },
        onSlideChange() {
            console.log('slide change')
        },
    },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    .page{
        width: 100%;
        min-height: 100vh;
    }
    .header{
        display: flex;
        padding: 0.5rem;
        img{
            display: inline-block;
            width: 25%;
            height: auto;
        }
    }

    .banner{
        .swiper{
            .slide-container{
                width: 100%;
                img{
                    display: block;
                    width: 100%;
                    height: auto;
                }
            }
        }
    }

    .list{
        position: relative;
        .more{
            position: relative;
            min-height: 10rem;
            background-repeat: no-repeat;
            background-size: 100% 100%;

            .content{
                padding: 5% 8%;
                text-align: start;
                color: white;
                div{
                    display: flex;
                    justify-content: space-between;
                }
            }
        }

        .more-item1{
            padding-top: 5%;
            background-image: url('../assets/more-bg1.png');
        }
        .more-item2{
            background-image: url('../assets/more-bg3.png');
        }

        .title{
            img{
                display: inline-block;
                width: 64%;
                height: auto;
            }
        }

        .divider{
            position: absolute;
            top: 60%;
            img{
                display: inline-block;
                width: 90%;
            }
        }
    }
</style>
