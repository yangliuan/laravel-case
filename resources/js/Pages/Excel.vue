<template>
    <app-layout title="Dashboard">
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">
                Excel
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
                            Laravel Excel 使用DEMO <a href="https://docs.laravel-excel.com/3.1/getting-started/" target="_blank">文档地址</a>
                        </div>

                        <div class="mt-6 text-gray-500">

                        </div>
                    </div>

                    <div class="bg-gray-200 bg-opacity-25 grid grid-cols-1 md:grid-cols-2">
                        <div class="p-6">
                            <div class="flex items-center">
                                <svg fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" viewBox="0 0 24 24" class="w-8 h-8 text-gray-400"><path d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.747 0 3.332.477 4.5 1.253v13C19.832 18.477 18.247 18 16.5 18c-1.746 0-3.332.477-4.5 1.253"></path></svg>
                                <div class="ml-4 text-lg text-gray-600 leading-7 font-semibold">Laravel Excel</div>
                            </div>

                            <div class="ml-12">
                                <div class="mt-2 text-sm text-gray-500">
                                    常用导入导出功能
                                </div>
                                <a href="/api/excel/export/store">
                                    <div class="mt-3 flex items-center text-sm font-semibold text-indigo-700">
                                            <div>导出到磁盘</div>
                                            <div class="ml-1 text-indigo-500">
                                                <svg viewBox="0 0 20 20" fill="currentColor" class="w-4 h-4"><path fill-rule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg>
                                            </div>
                                    </div>
                                </a>
                                <a href="/api/excel/export/download">
                                    <div class="mt-3 flex items-center text-sm font-semibold text-indigo-700">
                                            <div>下载导出</div>
                                            <div class="ml-1 text-indigo-500">
                                                <svg viewBox="0 0 20 20" fill="currentColor" class="w-4 h-4"><path fill-rule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg>
                                            </div>
                                    </div>
                                </a>
                                <a href="/api/excel/export/download-sheets">
                                    <div class="mt-3 flex items-center text-sm font-semibold text-indigo-700">
                                            <div>下载导出多页sheets</div>
                                            <div class="ml-1 text-indigo-500">
                                                <svg viewBox="0 0 20 20" fill="currentColor" class="w-4 h-4"><path fill-rule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg>
                                            </div>
                                    </div>
                                </a>
                                <a href="/api/excel/export/download-images">
                                    <div class="mt-3 flex items-center text-sm font-semibold text-indigo-700">
                                            <div>下载导出图片</div>
                                            <div class="ml-1 text-indigo-500">
                                                <svg viewBox="0 0 20 20" fill="currentColor" class="w-4 h-4"><path fill-rule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg>
                                            </div>
                                    </div>
                                </a>
                                <a href="/api/excel/export/queue">
                                    <div class="mt-3 flex items-center text-sm font-semibold text-indigo-700">
                                            <div>队列导出</div>
                                            <div class="ml-1 text-indigo-500">
                                                <svg viewBox="0 0 20 20" fill="currentColor" class="w-4 h-4"><path fill-rule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg>
                                            </div>
                                    </div>
                                </a>
                                <a href="#" @click="queueImagesClick">
                                    <div class="mt-3 flex items-center text-sm font-semibold text-indigo-700">
                                            <div>队列导出图片并用广播接受通知</div>
                                            <div class="ml-1 text-indigo-500">
                                                <svg viewBox="0 0 20 20" fill="currentColor" class="w-4 h-4"><path fill-rule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg>
                                            </div>
                                    </div>
                                </a>
                            </div>
                        </div>
                    </div>
                    <div class="bg-gray-200 bg-opacity-25 grid grid-cols-1 md:grid-cols-2">
                        <import-form />
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
    import ImportForm from '@/Jetstream/ImportForm.vue'
    import { Link } from '@inertiajs/inertia-vue3'
    import { echo } from '@/laravel-echo'

    export default defineComponent({
        components: {
            AppLayout,
            JetApplicationLogo,
            Link,
            ImportForm
        },
        created() {
            echo.channel('excel')
                .listen('ExcelExportCompletedEvent', (e) => {
                    alert('ExcelExportCompletedEvent')
                    this.downloadExcel(e.excel_path,e.disk)
                    console.log(e);
                })
        },
        methods: {
            downloadExcel(excel_path,disk) {
                const download_url =  '/api/files/download?storage_path=' + excel_path + '&disk=' + disk
                window.open(download_url)
            },
            queueImagesClick() {
                axios.post('/api/excel/export/queue-images').then( response => {
                    console.log(response)
                })
            }
        }
    })
</script>
