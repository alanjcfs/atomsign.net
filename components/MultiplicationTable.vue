<script setup>
const max = ref(12)
</script>
<template>
  <div>
      <table class="table-fixed mt-2 border border-solid border-spacing-2 text-center">
        <caption class="caption-top">
          {{ max }} x {{ max }} Multiplication Table
        </caption>
        <caption class="caption-bottom mt-4">
          <label for="number" class="block text-sm font-medium leading-6 text-gray-900">Number of rows and columns</label>
          <input
            name="number"
            id="number"
            class="block w-full rounded-md border-0 py-1.5 pl-3 text-gray-900 ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
            placeholder="12"
            type="number"
            v-model="max"
            min="1"
            max="100"
          />
        </caption>
        <tbody>
          <tr>
            <td class="border border-solid p-3"></td>
            <td v-for="i in max" class="border border-solid p-3">
              {{ i }}
            </td>
          </tr>
          <tr v-for="i in max">
            <td class="border border-solid p-3">
              {{ i }}
            </td>
            <td v-for="j in max" class="border border-solid p-3" :class="{ 'font-bold': i === j ? true : false }">
              {{ i * j }}
            </td>
          </tr>
        </tbody>
      </table>

    <div class="mt-8 mx-auto w-1/6 max-w-xs">
    </div>
  </div>
</template>
