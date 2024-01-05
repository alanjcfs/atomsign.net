<template>
  <div>
    <table class="table-fixed mt-2 border border-solid border-spacing-2 text-center">
      <caption class="caption-top">
        12x12
      </caption>
      <tbody>
        <tr v-for="i in 12">
          <td v-for="j in 12" class="border border-solid p-3" :class="{ 'font-bold': i * j === i || i * j === j ? false : true }">
            {{ i * j }}
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>
