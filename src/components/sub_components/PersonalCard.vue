<template>
        <div class="p-2 bg-gray-100 flex flex-col items-center justify-center rounded-md">
            <img :src="mediaUrl" alt="image from instagram" class="rounded-md h-auto">

            <div id="caption" class="font-semibold text-sm md:text-xl">
                {{caption}}
            </div>
        </div>
</template>

<script>
export default {
    props:{
        mediaUrl:{
            type: String
        },
        caption:{
            type: String
        }
    },
}
</script>

