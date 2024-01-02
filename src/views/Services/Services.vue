<template>
    <main>
        <div class="container mx-auto mt-[80px] lg:mt-[100px]">
            <div class="flex pb-10">
                <router-link to="/" class="text-[#ABABAB] font-[500] hidden md:block">{{ $t('translation.navbar.one') }}/</router-link>
                <router-link to="/services" class="font-[500] hidden md:block">{{ $t('translation.navbar.two') }}</router-link>
            </div>
            <h1 class="text-center md:w-[70%] mx-auto font-[700] text-[24px] md:text-[32px] text-[#333]">{{$t('translation.services.one')}}</h1>
            <p class="text-center md:w-[90%] mx-auto font-[700] text-[15px] md:text-[20px] text-[#666] mt-[20px]">{{$t('translation.services.two')}}</p>
        </div>
    </main>
</template>

<script setup>

</script>

<style lang="scss" scoped>

</style>