<script lang="ts" setup>
import {ref} from 'vue';

const count = ref(0);
</script>

<template>
  <el-button @click="count++">
    count is: {{ count }}
  </el-button>
  <br><br>
  <code>packages/renderer/src/components/ReactiveCounter.vue</code>
</template>
