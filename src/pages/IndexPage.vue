<template>
  <q-page>
    <div class="bg-primary q-pa-sm text-white">
      <div class="row">
        <div class="col-12 col-md-7">
          <p
            class="bg-secondary q-pa-sm rounded-borders"
            style="width: fit-content"
          >
            풀타임, 파트타임
          </p>
          <p class="text-weight-bolder text-h4">최고의 실력을 가진</p>
          <p class="text-weight-bolder text-h4">외국인 인재를 찾고 계신가요?</p>
          <p class="text-weight-bolder text-h4">인사관리</p>
          <p class="q-py-lg text-h5">
            법률 및 인사관리 부담없이 1주일 이내에 원격으로 채용해보세요.
          </p>
        </div>
        <div class="col-12 col-md-5">
          <ThreeDCarousel />
        </div>
      </div>
      <CheckList />
    </div>
    <div class="q-pt-xl q-pa-sm bg-grey-2">
      <div class="row">
        <div class="col-12 col-md-4">
          <img src="src/assets/brand_dark.png" alt="" />
          <p class="q-mt-lg text-weight-bolder">
            우리는 국가의 장벽을 넘어 최고의 인재를 매칭해드립니다.
          </p>
          <p class="text-weight-bold">010-0000-0000</p>
          <p class="text-weight-bold">aaaaa@naver.com</p>
        </div>
        <div class="col-12 col-md-8">
          <ListItem />
        </div>
      </div>
    </div>
  </q-page>
</template>

<script setup>
import ThreeDCarousel from "components/ThreeDCarousel.vue";
import CheckList from "components/CheckList.vue";
import ListItem from "src/components/ListItem.vue";
defineOptions({
  name: "IndexPage",
});
</script>
