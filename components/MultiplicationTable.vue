<template>
  <div>
    <table class="table-fixed border border-solid border-spacing-2 text-center">
      <caption class="caption-top">
        12x12
      </caption>
      <tbody>
        <tr v-for="i in 12">
          <td v-for="j in 12" class="border border-solid p-2">{{ i * j }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>
