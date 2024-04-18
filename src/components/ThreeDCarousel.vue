<template>
  <p class="top-tag"><q-icon name="monetization_on" /> 월 100만원</p>

  <swiper
    :effect="'cards'"
    :grabCursor="true"
    :modules="modules"
    class="mySwiper q-my-lg"
    :navigation="true"
  >
    <swiper-slide v-for="(slide, index) in slides" :key="index">
      <div class="text-center flex-center q-py-lg">
        <img :src="slide.img" alt="" class="q-mx-auto q-mb-lg" />
        <p class="text-h4 text-weight-bolder q-mb-sm">{{ slide.name }}</p>
        <p class="text-primary q-mb-lg">{{ slide?.experience }}</p>
        <div class="row flex-center q-gutter-sm">
          <p
            v-for="(tag, indexTag) in slide?.tags"
            :key="indexTag"
            class="tags"
          >
            {{ tag }}
          </p>
        </div>
      </div>
    </swiper-slide>
  </swiper>
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";
import "swiper/css/navigation";

import "swiper/css/effect-cards";

// import required modules
import { EffectCards, Navigation } from "swiper/modules";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [EffectCards, Navigation],
      slides: [
        {
          img: "src/assets/avatars/slideAvatar.png",
          name: "Tanzil Islam",
          experience: "마케팅 · 2y+",
          tags: [
            "마케팅 콘텐츠 제작",
            "인스타그램 관리",
            "트위터 관리",
            " 블로그 글 작성 ",
          ],
        },
        {
          img: "src/assets/avatars/slideAvatar.png",
          name: "Ujjal Roy",
          experience: "마케팅 · 3y+",
          tags: [
            "마케팅 콘텐츠 제작",
            "인스타그램 관리",
            "트위터 관리",
            " 블로그 글 작성 ",
          ],
        },
      ],
    };
  },
};
</script>
<style scoped>
.swiper {
  min-width: 240px;
  min-height: 320px;
  max-width: 400px;
}

.swiper-slide {
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 18px;
  font-size: 22px;
  font-weight: bold;
  color: black;
  background-color: #fff;
}
.tags {
  border: 1px solid gray;
  border-radius: 6px;
  padding: 4px 16px;
  color: gray;
  font-size: 12px;
  font-weight: bolder;
}
.top-tag {
  background-color: #fff;
  padding: 4px 18px;
  border-radius: 6px;
  color: green;
  width: fit-content;
  display: block;
  font-size: 22px;
  margin: auto;
  font-weight: bolder;
}
</style>
