<script setup>
const showMultiplicationTable = ref(false);

function toggleMultiplicationTable() {
  showMultiplicationTable.value = !showMultiplicationTable.value
}
</script>

<template>
  <UContainer>
    <UCard class="mt-4">
      <template #header>
        <div class="flex justify-between">
          <NuxtLink
            class="text-4xl font-bold"
            to="/"
          >Atom.</NuxtLink>

          <a
            class="text-4xl font-bold no-underline"
            href="https://github.com/alanjcfs"
          >
            Code.
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6 inline align-baseline">
                <path stroke-linecap="round" stroke-linejoin="round" d="M13.5 6H5.25A2.25 2.25 0 003 8.25v10.5A2.25 2.25 0 005.25 21h10.5A2.25 2.25 0 0018 18.75V10.5m-10.5 6L21 3m0 0h-5.25M21 3v5.25" />
              </svg>
          </a>

          <NuxtLink
            class="text-4xl font-bold no-underline"
            to="/american-sign-language">
            Sign.
          </NuxtLink>

          <ColorScheme>
            <USelect
              v-model="$colorMode.preference"
              :options="['system', 'light', 'dark']"
            />
          </ColorScheme>

        </div>
      </template>

      <div class="flex justify-between">
        <div
          @click="toggleMultiplicationTable"
          class="p-2 border rounded-sm cursor-pointer select-none"
        >Multiplication Table</div>
      </div>
      <Transition>
        <MultiplicationTable
          v-if="showMultiplicationTable"
        />
      </Transition>

    </UCard>

    <UCard class="mt-4">
      <NuxtPage class="prose prose-zinc dark:prose-invert" />
    </UCard>
  </UContainer>
</template>

<style scoped>
.v-enter-active,
.v-leave-active {
  transition: opacity 0.5s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}
</style>
