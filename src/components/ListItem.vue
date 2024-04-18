<template>
  <div class="q-mt-xl">
    <div class="row q-col-gutter-md">
      <div class="col-6 col-md-3" v-for="(item, index) in list" :key="index">
        <div class="bg-white q-pa-md border-radius" style="height: 100%">
          <q-icon
            :name="item?.icon"
            size="md"
            color="grey-5"
            class="bg-grey-2 q-pa-sm q-mb-md"
          ></q-icon>
          <p class="text-weight-bold">{{ item?.title }}</p>
          <div class="row items-center q-gutter-sm">
            <p>{{ item?.subtitle }}</p>
            <q-icon
              size="sm"
              color="grey-8"
              class="bg-grey-2 q-pa-sm q-mb-md border-radius"
              name="arrow_right_alt"
            ></q-icon>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const list = [
  { icon: "code", title: "해외 개발자 원격 채용", subtitle: "바로가기" },
  { icon: "person", title: "외국인 원격 채용 ", subtitle: "바로가기" },
  {
    icon: "settings",
    title: "한국어 가능 외국인 채용",
    subtitle: "해외 개발자 활용 서비스",
  },
  {
    icon: "code",
    title: "해외 개발자 원격 채용",
    subtitle: "바로가기",
  },
];
</script>

<style lang="scss" scoped></style>
