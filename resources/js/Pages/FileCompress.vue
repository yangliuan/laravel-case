<template>
    <app-layout title="Dashboard">
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">
                FileCompress
            </h2>
        </template>

        <div class="py-12">
            <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
                <div class="bg-white overflow-hidden shadow-xl sm:rounded-lg">
                    <div class="p-6 sm:px-20 bg-white border-b border-gray-200">
                        <div>
                            <jet-application-logo class="block h-12 w-auto" />
                        </div>

                        <div class="mt-8 text-2xl">
                            laravel-zipstream 使用DEMO <a href="https://github.com/stechstudio/laravel-zipstream" target="_blank">文档地址</a>
                        </div>

                        <div class="mt-6 text-gray-500">

                        </div>
                    </div>

                    <div class="bg-gray-200 bg-opacity-25 grid grid-cols-1 md:grid-cols-2">
                        <div class="p-6">
                            <div class="flex items-center">
                                <svg fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" viewBox="0 0 24 24" class="w-8 h-8 text-gray-400"><path d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.747 0 3.332.477 4.5 1.253v13C19.832 18.477 18.247 18 16.5 18c-1.746 0-3.332.477-4.5 1.253"></path></svg>
                                <div class="ml-4 text-lg text-gray-600 leading-7 font-semibold">laravel-zipstream</div>
                            </div>

                            <div class="ml-12">
                                <file-compress-form />
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </app-layout>
</template>

<script>
    import { defineComponent } from 'vue'
    import AppLayout from '@/Layouts/AppLayout.vue'
    import JetApplicationLogo from '@/Jetstream/ApplicationLogo.vue'
    import FileCompressForm from '@/Jetstream/FileCompressForm.vue'

    export default defineComponent({
        components: {
            AppLayout,
            JetApplicationLogo,
            FileCompressForm
        },
    })
</script>
