<script setup lang="ts">
  const progress = ref<number>(0);

  setTimeout(function() {
    progress.value = 88;
  }, 300)

</script>

<template>
  <div class="text-center">
    <h1 class="text-4xl my-8 font-semibold">Animated Circle Progress Bars</h1>
    <hr class="bg-gray-200 mb-8" />
    <p>Fully customizable Circle progress bar with animated </p>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-8">
      <div class="col-span-4">
        <RoundedProgressBar
          :progress="progress"
        />
      </div>
      <div>
        <RoundedProgressBar
          :progress="progress"
          :animation-duration="2000"
        />
      </div>
      <div>
        <RoundedProgressBar
          :progress="progress"
          :animation-duration="500"
          :decimal-places="2"
          :text-layout="'text-sm'"
        />
      </div>
      <div>
        <RoundedProgressBar
          :progress="progress"
          :animation-duration="800"
          :text-layout="'text-sm'"
          :radius="40"
          :progress-radius="25"
        />
      </div>
      <div>
        <RoundedProgressBar
          :progress="progress"
          :text-layout="'text-xl'"
          :thickness="8"
          :progress-thickness="8"
        />
      </div>
      <div>
        <RoundedProgressBar
          :progress="progress"
          :text-layout="'text-4xl font-bold text-red-800'"
          :container-width="'w-40'"
          :container-height="'h-40'"
          :radius="70"
          :progress-radius="70"
          :thickness="10"
          :progress-thickness="15"
          :cx="80"
          :cy="80"
          :progress-cx="80"
          :progress-cy="80"
        />
      </div>
      <div>
        <RoundedProgressBar
          :progress="progress"
          :text-layout="'text-4xl font-bold text-red-800'"
          :container-width="'w-40'"
          :container-height="'h-40'"
          :radius="70"
          :progress-radius="70"
          :thickness="10"
          :progress-thickness="4"
          :cx="80"
          :cy="80"
          :progress-cx="80"
          :progress-cy="80"
        />
      </div>
      <div>
        <RoundedProgressBar
          :progress="progress"
          :text-layout="'text-4xl font-bold text-white drop-shadow-lg'"
          :container-width="'w-40'"
          :container-height="'h-40'"
          :radius="70"
          :progress-radius="70"
          :thickness="0"
          :progress-thickness="140"
          :cx="80"
          :cy="80"
          :progress-cx="80"
          :progress-cy="80"
        />
      </div>
    </div>
  </div>
</template>