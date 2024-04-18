<template>
  <div class="q-my-lg row flex-wrap q-gutter-lg items-baseline">
    <div v-for="(item, index) in list" :key="index">
      <div class="row q-gutter-sm">
        <q-icon size="sm" name="check_box"></q-icon>
        <p class="text-weight-bolder">{{ item }}</p>
      </div>
    </div>
  </div>
  <p class="text-weight-bolder" style="color: yellow">개발자가 필요하신가요?</p>
</template>

<script setup>
const list = ["한국어 능력", "업무 수행 능력", "겸업 여부 ", "겸업 여부 "];
</script>

<style lang="scss" scoped></style>
