<template>
  <UContainer>
    <UCard class="mt-10">
      <template #header>
        <div class="flex justify-between">
          <div><a class="text-4xl font-bold" href="/">Atom.</a></div>

          <div><a class="text-4xl font-bold no-underline" href="https://github.com/alanjcfs">Code.</a></div>

          <div>
            <a
              class="text-4xl font-bold no-underline"
              href="/american-sign-language">
              Sign.
            </a>
          </div>
          <ColorScheme>
            <USelect
              v-model="$colorMode.preference"
              :options="['system', 'light', 'dark']"
            />
          </ColorScheme>
        </div>
      </template>
    </UCard>

    <UCard class="mt-10">
      <NuxtPage class="prose prose-zinc dark:prose-invert" />
    </UCard>
  </UContainer>
</template>
