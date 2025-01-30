<template>
    <section class="sec ending">
        <div class="ending__cont">
            <h2 class="tit">
                <span>Thank you</span>
            </h2>
            <div class="desc">
                <div class="name">
                    <h3>김현우</h3>
                    <p>Kim Hyeon woo</p>
                </div>
                <div class="email">
                    ekfvoddl0321@gmail.com
                </div>
            </div>
        </div>
    </section>
</template>
<script>
    import { gsap } from 'gsap';
    import { ScrollTrigger } from 'gsap/ScrollTrigger';

    gsap.registerPlugin(ScrollTrigger);

    export default {
        methods: {
            endingGsap() {
                let tl = gsap.timeline({
                    scrollTrigger: {
                        trigger: ".ending",
                        start: "20% center",
                        end: '-100%',
                        scrub: 4,
                    },

                })
                tl.from(".ending__cont .tit span", { opacity: 0, y: 100 })
                    .from(".ending__cont .desc", { opacity: 0, y: 50 }, .3)
                    .to(".project__item:nth-child(5)", { backgroundColor: '#eee9d6' }, 0)
                    .to(".project__item:nth-child(5) .project__img", { opacity: '0' }, 0)
                    .to(".project__info", { opacity: '0' }, 0)

            }
        },
        mounted() {
            this.endingGsap()
        },
    }
</script>
<style>

</style>