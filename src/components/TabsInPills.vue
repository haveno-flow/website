<template>
  <div>
    <div class="sm:hidden">
      <label for="tabs" class="sr-only">Select a tab</label>
      <select id="tabs" name="tabs" class="block w-full rounded-md border-gray-300 focus:border-indigo-500 focus:ring-indigo-500" @change="$emit('update:modelValue', $event.target.value)">
        <option v-for="tab in tabs" :key="tab" :value="tab" :selected="tab === modelValue">{{ tab }}</option>
      </select>
    </div>
    <div class="hidden sm:block">
      <nav class="flex space-x-4" aria-label="Tabs">
        <button
          v-for="tab in tabs"
          :key="tab"
          @click="$emit('update:modelValue', tab)"
          :class="[tab === modelValue ? 'bg-gray-100 text-gray-700' : 'text-gray-500 hover:text-gray-700', 'rounded-md px-3 py-2 text-sm font-medium']"
          :aria-current="tab === modelValue ? 'page' : undefined"
        >{{ tab }}</button>
      </nav>
    </div>
  </div>
</template>

<script setup>
defineProps({
  tabs: Array,
  modelValue: String,
})
defineEmits(['update:modelValue'])
</script>
