<script setup lang="ts">
  const progress = ref<number>(0);
  const customProgress = ref<string>('0');
</script>

<template>
  <div class="text-center">
    <h1 class="text-4xl my-8 font-semibold">Animated Circle Progress Bars</h1>
    <hr class="bg-gray-200 mb-8" />
    <p>Fully customizable <strong>Circle Progress Bar</strong> with animated data</p>
    <div class="grid grid-cols-1">
      <div>
        <CircleProgressBar
          :progress="progress"
        />
        <button
          :class="{'bg-gray-200': progress === 0, 'bg-gray-50': progress !== 0}"
          @click="progress = 0"
        >
          0%
        </button>
        <button
          :class="{'bg-gray-200': progress === 25, 'bg-gray-50': progress !== 25}"
          @click="progress = 25"
        >
          25%
        </button>
        <button
          :class="{'bg-gray-200': progress === 33, 'bg-gray-50': progress !== 33}"
          @click="progress = 33"
        >
          33%
        </button>
        <button
          :class="{'bg-gray-200': progress === 88, 'bg-gray-50': progress !== 88}"
          @click="progress = 88"
        >
          88%
        </button>
        <button
          :class="{'bg-gray-200': progress === 100, 'bg-gray-50': progress !== 100}"
          @click="progress = 100"
        >
          100%
        </button>
        <hr class="w-96 mx-auto my-8">
        <input
        v-model="customProgress" 
        />
        <button
          :class="{'bg-gray-200': progress === 100, 'bg-gray-50': progress !== 100}"
          @click="progress = parseFloat(customProgress)"
          >
          Set your own
        </button>
        <hr class="w-96 mx-auto my-8">
        <p>For more information about configuration and examples see our <NuxtLink class="text-blue-800" to="https://ui.santri.pl/circle-progress-bar/">Demo Page</NuxtLink></p>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  button, input {
    @apply shadow rounded px-5 py-2 mx-2 hover:bg-gray-200 transition-all duration-300
  }
  input {
    @apply w-16
  }
</style>