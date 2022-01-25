<template>

    <div class="flex flex-col mt-32 items-center justify-center">
        
        <div class="w-1/2 transition-colors flex flex-col">
            <div>
                <a class="text-4xl font-bold uppercase cursor-pointer programmer" target="_blank" href="https://github.com/Hasib-cirkut">Programmer</a>

                <p class="-ml-8 text-4xl cursor-pointer font-bold w-fit uppercase programmer">Movie Buff</p>
            </div>
            
            <img 
            class="rounded-md"
            src="/images/profile.jpg" alt="profile_pic">

            <div class="flex flex-col justify-end items-end">
                <p class="text-4xl cursor-pointer programmer font-bold -mr-8 uppercase">An Aesthete</p>

                <p class="text-4xl cursor-pointer programmer font-bold uppercase">Melophile</p>
            </div>
        </div>

    </div>

</template>

<script>


</script>

<style scoped>
.programmer{
    color: white;
    -webkit-text-fill-color: transparent;
    -webkit-text-stroke-width: 1px;
    -webkit-text-stroke-color: antiquewhite;
}

.programmer:hover{
    -webkit-text-fill-color: antiquewhite;
    -webkit-text-stroke-width: 0px;

}
</style>

