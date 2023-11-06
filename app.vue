<template>
  <UContainer>
    <UCard class="mt-10">
      <template #header>
        <div class="flex justify-between">
          <router-link to="/"><h1 class="text-2xl font-bold">Home</h1></router-link>
          <router-link to="/about"><h1 class="text-2xl font-bold">About</h1></router-link>
          <ColorScheme><USelect v-model="$colorMode.preference" :options="['system', 'light', 'dark']" /></ColorScheme>
        </div>
      </template>
    </UCard>
    <UCard class="mt-10">
      <NuxtPage />
    </UCard>
  </UContainer>
</template>
