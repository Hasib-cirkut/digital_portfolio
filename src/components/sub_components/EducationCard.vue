<template>
    <div class="flex flex-col md:w-1/2 h-40 rounded-md px-4 py-4 border-2 border-[#faebd7] text-gray-50 " :class="[bgInfo.margin]">
        <div class="flex-1">
        <p class="text-md md:text-2xl font-mono">{{info.label}}</p>
        <p class="font-semibold text-sm md:text-lg">{{info.desc}}</p>
        </div>

        <div>
        <p class="font-mono text-sm md:text-lg">{{info.timeline}}</p>
        </div>
    </div>
</template>

<script>
export default {

    props:{
        info:{
            type: Object
        },

        bgInfo:{
            type: Object
        }
    },

}
</script>

