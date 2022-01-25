<template>
    <div class="flex flex-col space-y-8 border-2 border-[#faebd7] text-gray-50 px-4 py-2 rounded-lg bg-no-repeat">
                <h2 class="text-2xl font-mono font-semibold">{{info.label}}</h2>

                <p class="text-gray-300 font-mono text-xl">{{info.desc}}</p>

                <p class="font-mono">
                    Created using
                    <span> <a href="#" class="hover:underline font-semibold decoration-blue-500">react</a> </span>,
                    <span>
                    <a href="#" class="hover:underline font-semibold decoration-orange-50">express</a>
                    </span>
                    and
                    <span> <a href="#" class="hover:underline font-semibold decoration-blue-700">tailwindcss</a> </span>.
                </p>

                <a href="#" class="hover:underline font-semibold decoration-pink-400 font-mono">live Link</a>
            </div>
</template>

<script>
export default {
    props:{
        info: Object,
    }
}
</script>

