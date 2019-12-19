<template>
    <div>
        <slick ref="slick" :options="slickOptions" class="slickText">
            <!-- <div v-for="(n,i) in data" :key="i">
                    <template v-if="getUserImage(n)">
                        <img :src="getUserImage(n)" class="slickImg"/>
                    </template> -->
            <div class="ma-1">
                <template>
                    <img src="@/assets/slider4.jpg" class="slickImg"/>
                </template>
                <p class="pa-0 ma-0 userName">asdfd asdfasd</p>
            </div>
            <div class="ma-1">
                <template>
                    <img src="@/assets/slider1.jpg" class="slickImg"/>
                </template>
                <p class="pa-0 ma-0 userName">asdfd asdfasd</p>
            </div>
            <div class="ma-1">
                <template>
                    <img src="@/assets/slider2.jpg" class="slickImg"/>
                </template>
                <p class="pa-0 ma-0 userName">asdfd asdfasd</p>
            </div>
   
            <!-- </div> -->
        </slick>
    </div>
</template>

<script>
    import Slick from "vue-slick";

    export default {
        name: "SlickCarouselNeighbours",
        components: {
            Slick
        },
        props: ["data", "option"],
        data() {
            return {
                slickOptions: {
                    infinite: true,
                    responsive: [
                        {
                            breakpoint: 1904,
                            settings: {
                                slidesToShow: 3,
                                slidesToScroll: 3,
                                infinite: true,
                                dots: true
                            }
                        },
                        {
                            breakpoint: 1264,
                            settings: {
                                slidesToShow: 3,
                                slidesToScroll: 3,
                                infinite: true,
                                dots: true
                            }
                        },
                    ]
                },
            }
        },
        methods: {
            getUserImage(data) {
                if (data && data.user && data.user.profilePic && data.user.profilePic.fileUrl) {
                    if (data.user.profilePic.fileUrl.includes('txt')) {
                        return false
                    } else {
                        return data.user.profilePic.fileUrl
                    }
                } else {
                    return false
                }
            },
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
            },
            getName(data) {
                if (data) {
                    const item = data.name.split(' ');
                    if (item[0].length > 7) {
                        return item[0].substr(0,5) + '...'
                    }else {
                        return item[0]
                    }
                } else {
                    return 'Buildo User'
                }
            },
        }
    }
</script>

<style scoped>
    .slickText {
        text-align: center;
    }

    .slickImg {
        height: 400px;
        width: 360px;
    }

    .userName {
        color: black;
        font-size: 20px;
        font-weight: bold
    }

    .slick-prev {
        left: -15px !important;
    }
</style>
