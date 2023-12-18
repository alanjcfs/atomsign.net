<template>
  <main>
    <ContentList path="/2023" v-slot="{ list }">
      <ul class="list-none">
        <li v-for="article in list" :key="article._path">
          <nuxt-link :to="article.path">{{ article.title }}</nuxt-link>
        </li>
      </ul>
    </ContentList>
  </main>
</template>
