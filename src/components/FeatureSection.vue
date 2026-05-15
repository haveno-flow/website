<template>
  <div id="download" class="mx-auto mt-16 max-w-7xl px-6 lg:px-8">
    <div class="mx-auto max-w-2xl lg:text-center">
      <h2 class="text-base font-semibold leading-7 text-indigo-600">Download</h2>
      <p class="mt-2 text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">Choose your platform</p>
      <p class="mt-6 text-lg leading-8 text-gray-600">Select your operating system and download the latest release.</p>
    </div>
    <div class="mx-auto mt-16 max-w-2xl sm:mt-20 lg:mt-24 lg:max-w-4xl">
      <dl class="grid max-w-xl grid-cols-1 gap-x-8 gap-y-10 lg:max-w-none lg:grid-cols-2 lg:gap-y-16">
        <div v-for="platform in platforms" :key="platform.name" class="relative pl-16">
          <dt class="text-base font-semibold leading-7 text-gray-900">
            <div class="absolute left-0 top-0 flex h-10 w-10 items-center justify-center rounded-lg bg-indigo-600">
              <component :is="platform.icon" class="h-6 w-6 text-white" aria-hidden="true" />
            </div>
            {{ platform.name }}
          </dt>
          <dd class="mt-2 text-base leading-7 text-gray-600">{{ platform.description }}</dd>
        </div>
      </dl>
      <div class="mt-16 text-center">
        <a href="#" class="text-sm font-semibold leading-6 text-indigo-600">View all releases on GitHub <span aria-hidden="true">&rarr;</span></a>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ComputerDesktopIcon, CommandLineIcon, ServerIcon, CpuChipIcon, CodeBracketIcon, CubeIcon } from '@heroicons/vue/24/outline'

const platforms = [
  {
    name: 'Debian',
    description: '.deb package for Debian 11 and later.',
    icon: CommandLineIcon,
  },
  {
    name: 'Ubuntu',
    description: '.deb package for Ubuntu 22.04 and later.',
    icon: ServerIcon,
  },
  {
    name: 'macOS',
    description: 'Universal binary for macOS 12 Monterey and later.',
    icon: ComputerDesktopIcon,
  },
  {
    name: 'Windows',
    description: 'Installer for Windows 10 and Windows 11.',
    icon: CpuChipIcon,
  },
  {
    name: 'Arch Linux',
    description: 'Available via the AUR for Arch-based distributions.',
    icon: CodeBracketIcon,
  },
  {
    name: 'Fedora',
    description: '.rpm package for Fedora 38 and later.',
    icon: CubeIcon,
  },
]
</script>
