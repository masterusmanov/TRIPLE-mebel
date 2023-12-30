<template>
    <footer class="mt-[112px] md:mt-[150px] xl:mt-[200px] bg-[#F5F5F6] py-[30px]">
        <div class="container mx-auto px-5 md:flex md:gap-[50px]">
            <div class="flex md:block md:w-[33%]">
                <div class="w-[100%] flex items-center gap-2 md:w-[100%]">
                    <img src="../../assets/images/mebelLogo.svg" alt="BrendLOGO" class="w-[100px]">
                </div>
                <p class="text-[16px] text-[#424259] font-[400] mt-[24px] font-rubik">{{$t('translation.main.footer.one')}}</p>
            </div>
            <div class="mt-[40px] md:w-[30%] md:mt-0 xl:ml-[180px]">
                <h2 class="text-[16px] font-[700] text-[#424259]">{{$t('translation.main.footer.two')}}</h2>
                <div class="grid gap-[16px] mt-[16px]">
                    <a href="#about" class="text-[16px] font-[400] text-[#424259] font-rubik">{{$t('translation.main.footer.three')}}</a>
                    <a href="#feature" class="text-[16px] font-[400] text-[#424259] font-rubik">{{$t('translation.main.footer.four')}}</a>
                    <a href="#patient" class="text-[16px] font-[400] text-[#424259] font-rubik">{{$t('translation.main.footer.five')}}</a>
                </div>
            </div>
            <div class="mt-[40px] md:w-[40%] md:mt-0">
                <h2 class="text-[16px] font-[700] text-[#424259] font-rubik">{{$t('translation.main.footer.six')}}</h2>
                <div class="grid gap-[16px] mt-[16px]">
                    <p class="text-[16px] font-[400] text-[#2588AF] font-rubik">+998 (99) 123-45-67</p>
                </div>
                <div class="mt-[24px]">
                    <h2 class="text-[16px] font-[700] text-[#424259] font-rubik">{{$t('translation.main.footer.seven')}}</h2>
                    <div class="flex items-center gap-6 mt-[24px]">
                        <a href="#"><i class='bx bxl-telegram text-[28px]'></i></a>
                        <a href="#"><i class='bx bxl-instagram text-[28px]'></i></a>
                        <a href="#"><i class='bx bxl-facebook-circle text-[28px]'></i></a>
                        <a href="#"><i class='bx bxl-youtube text-[28px]'></i></a>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<script setup>

</script>

<style lang="scss" scoped>

</style>