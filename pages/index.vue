<template>
  <button
      v-for="(item, idx) in locale"
      :key="idx"
      type="button"
      @click="navigateTo(switchLocalePath(item.code))"
  >
    {{ item.name }}
  </button>
  <div>{{ $t('test') }}</div>
</template>

<script setup lang="ts">
import locale from "~/utils/consts/locale";

const switchLocalePath = useSwitchLocalePath();
</script>

<style lang="scss" scoped>

</style>
