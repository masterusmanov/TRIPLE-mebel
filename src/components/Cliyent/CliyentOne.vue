<template>
    <section id="faq" class="px-2 lg:px-0 xl:px-4 2xl:px-0 mt-[80px] md:mt-[100px] xl:mt-[200px]">
        <div class="container mx-auto ">
            <h1 class=" font-[700] text-[24px] md:text-[32px] text-[#333]">{{$t('translation.main.cliyent.one')}}</h1>
            <p class="font-[700] text-[15px] md:text-[20px] text-[#666] mt-[27px] lg:w-[70%]">{{$t('translation.main.cliyent.two')}}</p>
        </div>
        <Cliyent class="mt-[40px] md:mt-[48px] xl:mt-[64px]"/>
    </section>
</template>

<script setup>
    import Cliyent from './Cliyent.vue';
</script>

<style lang="scss" scoped>

</style>