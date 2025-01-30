<template>
    <section class="sec kv">
        <div class="kv__text">
            <div class="kv__bg"></div>
            <ul class="kv__list">
                <li class="kv__item" v-for="(i, index) in 5" :key="index">
                    <div class="line"></div>
                </li>
            </ul>
            <div class="line"></div>

            <div class="text">
                <h1 class="tit">
                    <span class="item1">FRONTEND</span>
                    <span class="item2">2025 DEVELOPER SITE</span>
                </h1>
            </div>
        </div>
        <div class="kv__info">
            <ul class="kv__info-list">
                <li class="kv__info-item">FRONT-END DEVELOPER 2025</li>
                <li class="kv__info-item">KIM HYUN WOO</li>
            </ul>
            <div class="line"></div>
        </div>
    </section>


</template>
<script>
    import { gsap } from 'gsap';
    import { ScrollTrigger } from 'gsap/ScrollTrigger';

    gsap.registerPlugin(ScrollTrigger); // 전역적으로 등록

    export default {
        methods: {
            kvFn() {
                let tl = gsap.timeline();
                tl.from('.kv__list + .line', { scale: 0, duration: .7 }, 0)
                    .from('.kv__info-list + .line', { scale: 0, duration: .8 }, 0)
                    .from('.kv__item:nth-child(1) .line', { height: 0, duration: .3 })
                    .from('.kv__item:nth-child(2) .line', { height: 0, duration: .3 })
                    .from('.kv__item:nth-child(3) .line', { height: 0, duration: .4 })
                    .from('.kv__item:nth-child(4) .line', { height: 0, duration: .5 })
                    .from(".kv__bg", { opacity: .1, duration: 3, })
                    .to('.kv .line', { opacity: .3, duration: 3, delay: .5, })

                // gsap.from('.kv__info-list + .line', { scale: 0, duration: 1, delay: 1 });
                gsap.from('.kv__info-list', { y: 30, duration: 1, delay: 3, opacity: 0 });


                const textWrapper = this.$el.querySelector(".kv .text .tit .item1");
                if (textWrapper && textWrapper.textContent) {
                    textWrapper.innerHTML = textWrapper.textContent.replace(
                        /([\w\u0080-\uFFFF])/g,
                        "<span class='letter'>$&</span>"
                    );
                }
                const textWrapper2 = this.$el.querySelector(".kv .text .tit .item2");
                if (textWrapper2 && textWrapper2.textContent) {
                    textWrapper2.innerHTML = textWrapper2.textContent.replace(
                        /([\w\u0080-\uFFFF])/g,
                        "<span class='letter'>$&</span>"
                    );
                }

                gsap.from(".kv .text .tit .item1 .letter", { opacity: 0, x: 150, duration: 1, delay: 2.4, stagger: 0.1, });
                gsap.from(".kv .text .tit .item2 .letter", { opacity: 0, x: 150, duration: 1, delay: 2.6, stagger: 0.1, });
            }
        },
        mounted() {
            this.kvFn()
        },

    }
</script>