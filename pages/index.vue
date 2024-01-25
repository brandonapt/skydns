<script setup>
const buttonText = ref("44.219.64.20")
function copy() {
    copyToClipboard('44.219.64.20')
    buttonText.value = "Copied!"
    setTimeout(() => {
        buttonText.value = "44.219.64.20"
    }, 1000)
}

async function copyToClipboard(textToCopy) {
    // Navigator clipboard api needs a secure context (https)
    if (navigator.clipboard && window.isSecureContext) {
        await navigator.clipboard.writeText(textToCopy);
    } else {
        // Use the 'out of viewport hidden text area' trick
        const textArea = document.createElement("textarea");
        textArea.value = textToCopy;
            
        // Move textarea out of the viewport so it's not visible
        textArea.style.position = "absolute";
        textArea.style.left = "-999999px";
            
        document.body.prepend(textArea);
        textArea.select();

        try {
            document.execCommand('copy');
        } catch (error) {
            console.error(error);
        } finally {
            textArea.remove();
        }
    }
}
</script>

<template>
    <div class="relative text-center top-1/3">
        <h1 class="text-white font-bold text-7xl">SKYDNS</h1>
        <h3 class="text-white font-semibold text-xl">Bringing Skylanders mobile back</h3>
        <div class="flex justify-center mt-10">
            <a @click="copy" target="_blank" class="cursor-pointer bg-white hover:bg-gray-100 text-gray-800 font-semibold py-2 px-4 border border-gray-400 rounded shadow">
                {{ buttonText }}
                <Icon name="material-symbols:content-copy-outline" size="24" class="mt-n2" color="black" />
            </a>
            </div>
    </div>
</template>