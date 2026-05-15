<template>
  <div class="bg-white">
    <div class="mx-auto max-w-7xl px-6 py-24 sm:py-32 lg:px-8 lg:py-40">
      <div class="mx-auto max-w-4xl divide-y divide-gray-900/10">
        <h2 id="faq" class="text-2xl font-bold leading-10 tracking-tight text-gray-900">Frequently Asked Questions</h2>
        <div>
          <TabsInPills :tabs="tabNames" v-model="activeTab" class="mt-10" />
          <dl class="mt-6 space-y-6 divide-y divide-gray-900/10">
            <Disclosure as="div" v-for="faq in displayedFaqs" :key="faq.question" class="pt-6 pb-6" v-slot="{ open }">
              <dt>
                <DisclosureButton class="flex w-full items-start justify-between text-left text-gray-900">
                  <span class="text-base font-semibold leading-7">{{ faq.question }}</span>
                  <span class="ml-6 flex h-7 items-center">
                    <PlusIcon v-if="!open" class="h-6 w-6" aria-hidden="true" />
                    <MinusIcon v-else class="h-6 w-6" aria-hidden="true" />
                  </span>
                </DisclosureButton>
              </dt>
              <DisclosurePanel as="dd" class="mt-3 pr-12">
                <p class="text-base leading-7 text-gray-700" v-html="faq.answer"></p>
              </DisclosurePanel>
            </Disclosure>
          </dl>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue'
import { Disclosure, DisclosureButton, DisclosurePanel } from '@headlessui/vue'
import { MinusIcon, PlusIcon } from '@heroicons/vue/24/outline'
import TabsInPills from './TabsInPills.vue'
import rawFaqs from '../data/faq.md?raw'

const tabNames = ['All', 'Getting Started', 'Security & Privacy', 'Other']
const activeTab = ref('All')

const faqs = rawFaqs
  .split(/(?=^## )/m)
  .filter(s => s.trim())
  .map(section => {
    const newline = section.indexOf('\n')
    const question = section.slice(0, newline).replace(/^## /, '').trim()
    let body = section.slice(newline + 1).trimStart()
    let tags = []
    const tagsMatch = body.match(/^tags:[ \t]*(.+)\n?/)
    if (tagsMatch) {
      tags = tagsMatch[1].split(',').map(t => t.trim()).filter(Boolean)
      body = body.slice(tagsMatch[0].length)
    }
    const answer = body.trim()
      .replace(/\*\*(.+?)\*\*/g, '<strong class="block mt-4 mb-2 text-sm font-semibold uppercase tracking-wide text-gray-500">$1</strong>')
      .replace(/\[([^\]]+)\]\(([^)]+)\)/g, '<a href="$2" target="_blank" class="underline text-gray-900 hover:text-gray-600">$1</a>')
      .replace(/((?:^- .+$\n?)+)/gm, match => {
        const items = match.trim().split('\n').map(l => `<li>${l.slice(2)}</li>`).join('')
        return `<ul class="list-disc list-inside mt-2 mb-3 space-y-1">${items}</ul>`
      })
      .replace(/\n\n+/g, '<br><br>')
      .replace(/<\/strong><br><br>/g, '</strong>')
      .replace(/<br><br>(<ul)/g, '$1')
    return { question, answer, tags }
  })

const displayedFaqs = computed(() => {
  if (activeTab.value === 'All') return faqs
  return faqs.filter(faq => faq.tags.includes(activeTab.value))
})
</script>
