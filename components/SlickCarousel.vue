<template>
    <div>
        <slick ref="slick" :options="slickOptions" class="slickText">
            <div v-for="(item,i) in slickItems" :key="i" class="ma-1">
                <template>
                    <img :src="item.img" class="slickImg"/>
                </template>
                <p class="pa-0 ma-1 userName">{{ item.name }}</p>
            </div>
        </slick>
    </div>
</template>

<script>
    import Slick from "vue-slick";

    import slider1 from '@/assets/slider1.jpg'
    import slider2 from '@/assets/slider2.jpg'
    import slider3 from '@/assets/slider3.jpg'
    import slider4 from '@/assets/slider4.jpg'
    import slider5 from '@/assets/slider1.jpg'

    export default {
        name: "SlickCarouselNeighbours",
        components: {
            Slick
        },
        data() {
            return {
                slickOptions: {
                    infinite: true,
                    responsive: [
                        {
                            breakpoint: 1904,
                            settings: {
                                slidesToShow: 3,
                                slidesToScroll: 2,
                                infinite: true,
                                dots: true
                            }
                        },
                        {
                            breakpoint: 1264,
                            settings: {
                                slidesToShow: 2,
                                slidesToScroll: 1,
                                infinite: true,
                                dots: true
                            }
                        },
                        {
                            breakpoint: 960,
                            settings: {
                                slidesToShow: 1,
                                slidesToScroll: 1,
                                infinite: true,
                                dots: true
                            }
                        },
                    ]
                },

                slickItems: [
                    {id: 1, img: slider1, name: 'Slider One'},
                    {id: 2, img: slider2, name: 'Slider Two'},
                    {id: 3, img: slider3, name: 'Slider Three'},
                    {id: 4, img: slider4, name: 'Slider Four'},
                    {id: 5, img: slider5, name: 'Slider Five'}
                ]
            }
        },
        methods: {
            next() {
                this.$refs.slick.next();
            },

            prev() {
                this.$refs.slick.prev();
            },

            reInit() {
                // Helpful if you have to deal with v-for to update dynamic lists
                this.$nextTick(() => {
                    this.$refs.slick.reSlick();
                });
            }
        }
    }
</script>

<style scoped>
    .slickText {
        text-align: center;
    }

    .slickImg {
        height: 400px;
        width: 375px;
    }

    .userName {
        color: black;
        font-size: 18px;
        font-weight: bold
    }

    .slick-prev {
        left: -15px !important;
    }
</style>
