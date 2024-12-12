<template>
    <div as="nav" class="bg-danger">
        <div class="mx-auto px-2 sm:px-6 ">
            <div class="relative flex h-28 items-center justify-between">
                <div class="flex flex-1 h-20 items-center justify-center sm:items-stretch sm:justify-start">
                    <div class="flex shrink-0 items-center">
                        <img class="h-20 w-auto" src="/assets/images/logo.jpg" alt="Your Company" />
                    </div>
                    <div class="hidden sm:ml-6 sm:block">
                        <div class="flex pt-5 pb-5">
                            <h1 class="font-bold text-lg text-white">
                                ASPIRE WORLD IMMIGRATION SERVICES
                            </h1>
                        </div>
                    </div>
                    <div class="ms-40 bg-danger justify-between">
                        <TabGroup as="div" class=" mb-5 gap-10">
                            <TabList class="gap-10 mb-5 mt-3 flex font-light text-xl text-white">
                                <div v-for="nav in navigation">
                                    <Tab as="template">
                                        <a class=" flex items-center  p-7 py-3 !outline-none ">
                                            <!-- <icon-home class="size-6 text-white ltr:mr-2 rtl:ml-2 " /> -->
                                            {{ nav.name }}
                                        </a>
                                    </Tab>
                                </div>
                            </TabList>
                        </TabGroup>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import { TabGroup, TabList, Tab } from '@headlessui/vue'

const navigation = [
    { name: 'HOME', href: '#', current: true },
    { name: 'IMMIGRATION', href: '#', current: false },
    { name: 'ABOUT', href: '#', current: false },
    { name: 'CITIZENSHIP', href: '#', current: false },
    { name: 'CONTACT US', href: '#', current: false },
]
</script>
