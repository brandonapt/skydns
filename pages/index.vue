<script setup>
function copy() {
    navigator.clipboard.writeText('3.19.484.24')
}
</script>

<template>
    <div class="relative text-center top-1/3">
        <h1 class="text-white font-bold text-7xl">SKYDNS</h1>
        <h3 class="text-white font-semibold text-xl">Bringing Skylanders mobile back</h3>
        <div class="flex justify-center mt-10">
            <a @click="copy" target="_blank" class="cursor-pointer bg-white hover:bg-gray-100 text-gray-800 font-semibold py-2 px-4 border border-gray-400 rounded shadow">
                3.19.484.24
                <Icon name="material-symbols:content-copy-outline" size="24" class="mt-n2" color="black" />
            </a>
            </div>
    </div>
</template>