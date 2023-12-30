<script setup>
    import SectionTwo from '../components/SectionTwo/SectionTwo.vue'
</script>

<template>
    <main class="bg-[#EFEFEF] mt-[10px]">
        <div class="container mx-auto relative">
            <div class="md:bg-[#DFE9F4] font-mont md:absolute rounded-lg mt-[25px] py-[17px] md:px-[24px] md:py-[22px] lg:px-[29px] lg:py-[27px] xl:px-[34px] xl:py-[32px] 2xl:px-[39px] 2xl:py-[37px] md:w-[350px] lg:w-[500px]  xl:w-[600px] 2xl:w-[643px] md:mt-[70px] md:ml-[380px] lg:mt-[110px] lg:ml-[530px] xl:mt-[110px] xl:ml-[600px] 2xl:mt-[170px] 2xl:ml-[800px]">
                <p class="text-[#333] w-[70%] md:w-full mx-auto text-[12px] md:text-[16px] font-[600] lg:tracking-[3px]">{{$t('translation.main.one')}}</p>
                <h1 class="text-[#054C73] border text-[20px] w-[70%] md:w-full mx-auto md:text-[30px] lg:text-[35px] xl:text-[48px] 2xl:text-[52px] font-[700] xl:leading-[65px] mt-[5px] lg:mt-[10px] xl:mt-[15px] 2xl:mt-[20px]">{{$t('translation.main.two')}}</h1>
                <p class="text-[#333] text-[12px] lg:text-[14px] xl:text-[16px] 2xl:text-[18px] font-[500] xl:leading-[39px] w-[250px] mx-auto md:mx-0 md:w-[280px] lg:w-[400px] lg:h-[50px] xl:w-[500px] xl:h-[72px] 2xl:w-[546px] 2xl:h-[76px] mt-[5px] lg:mt-[10px] xl:mt-[15px] 2xl:mt-[20px]">{{$t('translation.main.three')}}</p>
                <div class="mt-[20px] lg:mt-[25px] xl:mt-[45px] 2xl:mt-[50px] w-[70%] md:w-full mx-auto ">
                    <router-link to="/contact" class="px-[30px] py-[10px] md:px-[40px] md:py-[10px] lg:px-[50px] lg:py-[15px] xl:px-[65px] xl:py-[20px] 2xl:px-[72px] 2xl:py-[25px] bg-[#054C73] rounded-full text-white font-[700] text-[12px] xl:text-[14px] 2xl:text-[16px]">{{$t('translation.main.four')}}</router-link>
                </div>
            </div>
            <img src="../assets/images/mainbg.png" alt="" class="">
            <div class="grid items-center gap-6 md:gap-9 lg:gap-[100px] 2xl:gap-[170px] md:flex py-[34px] justify-between xl:w-[95%] mx-auto">
                <div class="flex items-center gap-3 xl:gap-4 px-4 md:px-0">
                    <img src="../assets/images/main1/1.svg" alt="Delivery" class="w-[48px] md:w-[40px] lg:w-[56px]">
                    <div class="font-mont">
                        <h2 class="text-[18px] md:text-[14px] lg:text-[18px] xl:text-[24px] font-[600] text-[#333] tracking-[2px]">{{ $t('translation.main.delivery.one') }}</h2>
                        <p class="text-[14px] lg:text-[16px] font-[400] text-[#333]">{{ $t('translation.main.delivery.two') }}</p>
                    </div>
                </div>
                <div class="flex items-center xl:gap-4 gap-3 px-4 md:px-0">
                    <img src="../assets/images/main1/2.svg" alt="Delivery" class="w-[48px] md:w-[40px] lg:w-[56px]">
                    <div class="font-mont">
                        <h2 class="text-[18px] md:text-[14px] lg:text-[18px] xl:text-[24px] font-[600] text-[#333] tracking-[2px]">{{ $t('translation.main.delivery.three') }}</h2>
                        <p class="text-[14px] lg:text-[16px] font-[400] text-[#333]">{{ $t('translation.main.delivery.two') }}</p>
                    </div>
                </div>
                <div class="flex items-center xl:gap-4 gap-3 px-4 md:px-0">
                    <img src="../assets/images/main1/3.svg" alt="Delivery" class="w-[48px] md:w-[40px] lg:w-[56px]">
                    <div class="font-mont">
                        <h2 class="text-[18px] md:text-[14px] lg:text-[18px] xl:text-[24px] font-[600] text-[#333] tracking-[2px]">{{ $t('translation.main.delivery.four') }}</h2>
                        <p class="text-[14px] lg:text-[16px] font-[400] text-[#333]">{{ $t('translation.main.delivery.two') }}</p>
                    </div>
                </div>
            </div>
        </div>
    </main>
    <SectionTwo/>
</template>

<style scoped>
</style>
