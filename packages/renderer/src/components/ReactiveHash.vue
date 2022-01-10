<script lang="ts" setup>
import {computed, ref} from 'vue';

const rawString = ref('Hello World');
/**
 * window.nodeCrypto was exposed from {@link module:preload}
 */
const hashedString = computed(() => window.nodeCrypto.sha256sum(rawString.value));
</script>

<template>
  <label>
    Raw value
    <el-input
      v-model="rawString"
      type="text"
    />
  </label>
  <br>
  <label>
    Hashed by node:crypto
    <el-input
      v-model="hashedString"
      type="text"
      readonly
    ></el-input>
  </label>
  <br><br>
  <code>packages/renderer/src/components/ReactiveHash.vue</code>
</template>
