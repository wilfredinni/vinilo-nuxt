<script setup lang="ts">
import { Switch } from '@headlessui/vue'

useHead({
  title: 'Nuxt starter template - Vinilo',
  meta: [{ name: 'description', content: 'My amazing site.' }]
})

const enabled = ref(false)
</script>

<template>
  <div class="text-center">
    <Icon name="uil:github" />
    <h1 class="mb-5 text-4xl font-bold text-blue-500">Home</h1>
    <Switch
      v-model="enabled"
      :class="[
        enabled ? 'bg-indigo-600' : 'bg-gray-200',
        's relative inline-flex h-6 w-11 flex-shrink-0 cursor-pointer rounded-full border-2 border-transparent transition-colors duration-200 ease-in-out focus:outline-none focus:ring-2 focus:ring-indigo-600 focus:ring-offset-2'
      ]"
    >
      <span class="sr-only">Use setting</span>
      <span
        aria-hidden="true"
        :class="[
          enabled ? 'translate-x-5' : 'translate-x-0',
          'pointer-events-none inline-block h-5 w-5 transform rounded-full bg-white shadow ring-0 transition duration-200 ease-in-out'
        ]"
      />
    </Switch>
  </div>
</template>
