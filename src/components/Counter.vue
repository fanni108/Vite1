<script setup lang="ts">
  import { ref, computed } from 'vue'

  const count = ref < number > (0)
  const doubled = computed(() => count.value * 2)
  const magic = computed(() => {
    if (count.value % 2 === 0) {
      return 'even'
    } else {
      return 'odd'
    }
  })

</script>

<template>
  <div class="counter-container">
    <div class="counter-display">
      <span class="counter-value">{{ count }}</span>
    </div> 
  <button class="ButtonCounter" @click="count--">
    -
  </button>
  <button class="ButtonCounter" @click="count++">
    +
  </button>
  <div class="counter-magic">
  <span>Die Zahl ist: {{ magic }}</span>
  </div>
  </div>
  <div class="counter-container">
  <div class="counter-doubled">
  <span>Das doppelte ist: {{ doubled }}</span>
  </div>
  </div>

</template>