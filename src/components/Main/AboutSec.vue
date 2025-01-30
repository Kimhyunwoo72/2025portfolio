<template>
    <section class="sec about">
        <div class="main-title">
            <div class="inner">
                <h2 class="tit t-r">
                    <span>FRONTEND</span>
                    <span>About Me</span>
                </h2>
            </div>
        </div>
        <div class="about__wrap">
            <div class="line"></div>
            <div class="about__cont">
                <div class="about__img">
                    <div class="about__img-bg"></div>
                    <img src="@/assets/img/about-img.jpg" alt="">
                </div>
                <div class="about__text">
                    <ul class="about__list">
                        <li class="about__item item1">
                            <div class="text">
                                <div class="num num1">1.</div>
                                <p class="desc desc1">
                                    주어진 시간 내 프로젝트를 완수하는 것을 최우선으로 하며, 과정 속에서의 원활한 협업을 가장 중요하게 생각합니다. 지난 2년 반 동안 동료들과 한 번의 불화 없이 모든 프로젝트를 성공적으로 마무리했으며, 이는 저의 가장 큰 강점입니다.
                                </p>
                            </div>
                            <div class="line2 mo-none"></div>
                            <div class="line pc-none"></div>
                        </li>
                        <li class="about__item item2">
                            <div class="text">
                                <div class="num num2">2.</div>
                                <p class="desc desc2">
                                   반응형 웹, GSAP를 활용한 애니메이션, 웹 접근성을 고려한 마크업에 강점을 갖고 있으며, JavaScript, Vue, React를 사용한 프로젝트 경험이 다수 있습니다. 또한, API를 활용한 프론트엔드 개발 경험도 다양하게 보유하고 있습니다.
                                </p>
                            </div>
                            <div class="line2 mo-none"></div>
                            <div class="line pc-none"></div>
                        </li>
                        <li class="about__item item3">
                            <div class="text">
                                <div class="num num3">3.</div>
                                <p class="desc desc3">
                                    주 업무는 퍼블리셔였지만, 다양한 라이브러리와 프레임워크를 활용하며 프론트엔드 개발자로 꾸준히 성장하는 것을 목표로 하고 있습니다.
                                </p>
                            </div>
                            <div class="line2 mo-none"></div>
                            <div class="line pc-none"></div>
                        </li>

                    </ul>
                </div>
            </div>
            <div class="line mo-none"></div>
        </div>
    </section>
</template>
<script>
    import { gsap } from 'gsap';
    import { ScrollTrigger } from 'gsap/ScrollTrigger';

    gsap.registerPlugin(ScrollTrigger); // 전역적으로 등록

    export default {
        methods: {
            aboutGsap() {
                // title
                gsap.from(".about .main-title .tit span:first-child", { scrollTrigger: { trigger: ".about", start: "top 60%", }, ease: "power4.out", duration: 3, opacity: 0, x: 200 });
                gsap.from(".about .main-title .tit span:last-child", { scrollTrigger: { trigger: ".about", start: "top 60%", }, ease: "power4.out", duration: 4, delay: .2, opacity: 0, x: 200 });

                // line
                const tl = gsap.timeline({
                    scrollTrigger: {
                        trigger: ".about", // 트리거 요소
                        start: "top 30%", // 애니메이션 시작 지점
                    },
                });
                tl.from('.about .line', { scale: 0, duration: 1 }, 0)
                    .from('.about .line2', { scale: 0, duration: 1.3 }, .4)
                    .to('.about .about__img img', { duration: 5, scale: 1.1, })
                    .to('.about .line', { opacity: .3, duration: 3 }, 1)
                    .to('.about .line2', { opacity: .3, duration: 3 }, 1)
                    .to('.about .about__img-bg', { duration: 1.2, height: 0, }, .1)
                    .from('.about .num1', { duration: 1.2, x: -100, opacity: 0 }, .2)
                    .from('.about .num2', { duration: 1.2, x: -100, opacity: 0 }, .5)
                    .from('.about .num3', { duration: 1.2, x: -100, opacity: 0 }, .8)
                    .from('.about .desc1', { duration: 2, x: -20 + '%', opacity: 0 }, 1)
                    .from('.about .desc2', { duration: 2, x: -20 + '%', opacity: 0 }, 1.3)
                    .from('.about .desc3', { duration: 2, x: -20 + '%', opacity: 0 }, 1.6)

                // text

            }
        },
        mounted() {
            this.aboutGsap()
        },
    }
</script>
<style>

</style>