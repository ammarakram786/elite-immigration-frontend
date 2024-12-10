<template>
    <Disclosure as="nav" class="bg-light-800" v-slot="{ open }">
        <div class="mx-auto px-2 sm:px-6 ">
            <div class="relative flex h-28 items-center justify-between">
                <div class="absolute inset-y-0 left-0 flex items-center sm:hidden">
                    <!-- Mobile menu button-->
                    <DisclosureButton
                        class="relative inline-flex items-center justify-center rounded-md p-2 text-gray-400 hover:bg-gray-700 hover:text-white focus:outline-none focus:ring-2 focus:ring-inset focus:ring-white">
                        <span class="absolute -inset-0.5" />
                        <span class="sr-only">Open main menu</span>
                        <!-- <Bars3Icon v-if="!open" class="block size-6" aria-hidden="true" /> -->
                        <!-- <XMarkIcon v-else class="block size-6" aria-hidden="true" /> -->
                        <icon-bell-bing v-if="!open" class="block size-6" aria-hidden="true" />
                        <icon-bell-bing v-else class="block size-6" aria-hidden="true" />
                    </DisclosureButton>
                </div>
                <div class="flex flex-1 h-20 items-center justify-center sm:items-stretch sm:justify-start">
                    <div class="flex shrink-0 items-center">
                        <img class="h-20 w-auto" src="/assets/images/logo.jpg" alt="Your Company" />
                    </div>
                    <div class="hidden sm:ml-6 sm:block">
                        <div class="flex pt-5 pb-5">
                            <h1 class="font-bold text-lg">
                                ASPIRE WORLD IMMIGRATION SERVICES
                            </h1>
                        </div>
                    </div>
                    <div class="hidden sm:ml-6 sm:block">
                        <div class="px-5 flex space-x-8 pt-5 pb-5">
                            <a v-for="item in navigation" :key="item.name" :href="item.href"
                                :class="['text-dark hover:bg-primary-light hover:text-dark', 'rounded-md px-6 py-3 text-xl font-medium']"
                                :aria-current="item.current ? 'page' : undefined">{{ item.name }}</a>
                        </div>
                    </div>

                </div>
            </div>
        </div>

        <DisclosurePanel class="sm:hidden">
            <div class="space-y-1 px-2 pb-3 pt-5 ">
                <DisclosureButton v-for="item in navigation" :key="item.name" as="a" :href="item.href"
                    :class="[item.current ? 'bg-white-900 text-white' : 'text-gray-300 hover:bg-red-700 hover:text-white', 'block rounded-md px-3 py-2 text-base font-medium']"
                    :aria-current="item.current ? 'page' : undefined">{{ item.name }}</DisclosureButton>
            </div>
        </DisclosurePanel>
    </Disclosure>
</template>

<script setup>
import { Disclosure, DisclosureButton, DisclosurePanel } from '@headlessui/vue'

const navigation = [
    { name: 'Home', href: '#', current: true },
    { name: 'Immigration', href: '#', current: false },
    { name: 'About', href: '#', current: false },
    { name: 'citizenship', href: '#', current: false },
]
</script>
