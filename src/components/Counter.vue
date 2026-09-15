<script setup lang="ts">
  import { ref, computed } from 'vue'

  const count = ref < number > (0)
  const doubled = computed(() => count.value * 2)

</script>

<template>
  <span>Count ist: {{ count }}</span>
  <button class="counter" @click="count++">
    +
  </button>
  <button class="counter" @click="count--">
    -
  </button>
  <span>Das doppelte ist: {{ doubled }}</span>
</template>