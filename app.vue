<template>
  <UContainer>
    <UCard class="mt-10">
      <template #header>
        <div class="flex justify-between">
          <nuxt-link
            class="text-4xl font-bold"
            to="/"
          >Atom.</nuxt-link>

          <a
            class="text-4xl font-bold no-underline"
            to="//github.com/alanjcfs"
          >Code.</a>

          <nuxt-link
            class="text-4xl font-bold no-underline"
            to="/american-sign-language">
            Sign.
          </nuxt-link>
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
