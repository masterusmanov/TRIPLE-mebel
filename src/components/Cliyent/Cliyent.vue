<template>
    <div class=" container mx-auto relative">
        <div class="slides-container h-72 flex snap-x snap-mandatory overflow-hidden overflow-x-auto space-x-6 rounded scroll-smooth before:w-[45vw] before:shrink-0 after:w-[45vw] after:shrink-0 md:before:w-0 md:after:w-0" ref="slidesContainer">
            <div class="w-[325px] h-[285px] mx-auto rounded-[16px] border md:w-[350px] lg:w-[325px] xl:w-[400px] 2xl:w-[490px] xl:h-[242px] 2xl:h-[232px] slide aspect-square  flex-shrink-0 snap-center overflow-hidden">
                <div class=" mt-[24px] h-[180px] xl:h-[140px] 2xl:h-[120px]">
                    <p class="text-[16px] px-4 text-justify font-rubik">{{$t('translation.main.cliyent.three')}}</p>
                </div>
                <div class="flex items-center gap-4 pt-4">
                    <img src="../../assets/images/cliyent/Ellipse 8.png" alt="icon" class="w-[44px] h-[44px] md:mx-0 ml-3 md:ml-3 md:mt-2 lg:mt-0">
                    <div class="">
                        <h2 class="text-[16px] font-[700] font-rubik">Xojiakbar To'raxo'jayev</h2>
                    </div>
                </div>
            </div>
            <div class="w-[325px] h-[285px] mx-auto rounded-[16px] border md:w-[350px] lg:w-[325px] xl:w-[400px] 2xl:w-[490px] xl:h-[242px] 2xl:h-[232px] slide aspect-square  flex-shrink-0 snap-center overflow-hidden">
                <div class=" mt-[24px] h-[180px] xl:h-[140px] 2xl:h-[120px]">
                    <p class="text-[16px] px-4 text-justify font-rubik">{{$t('translation.main.cliyent.four')}}</p>
                </div>
                <div class="flex items-center gap-4 pt-4">
                    <img src="../../assets/images/cliyent/Ellipse 2.png" alt="icon" class="w-[44px] h-[44px] md:mx-0 ml-3 md:ml-3 md:mt-2 lg:mt-0">
                    <div class="">
                        <h2 class="text-[16px] font-[700] font-rubik">Aziz Yusupov</h2>
                    </div>
                </div>
            </div>
            <div class="w-[325px] h-[285px] mx-auto rounded-[16px] border md:w-[350px] lg:w-[325px] xl:w-[400px] 2xl:w-[490px] xl:h-[242px] 2xl:h-[232px] slide aspect-square  flex-shrink-0 snap-center overflow-hidden">
                <div class="">
                    <div class=" mt-[24px] h-[180px] xl:h-[140px] 2xl:h-[120px]">
                        <p class="text-[16px] px-4 text-justify font-rubik">{{$t('translation.main.cliyent.five')}}</p>
                    </div>
                    <div class="flex items-center gap-4 pt-4">
                        <img src="../../assets/images/cliyent/Ellipse 1.png" alt="icon" class="w-[44px] h-[44px] md:mx-0 ml-3 md:ml-3 md:mt-2 lg:mt-0">
                        <div class="">
                            <h2 class="text-[16px] font-[700] font-rubik">Dilnoza Xakimova</h2>
                        </div>
                    </div>
                </div>
            </div>
        </div>

       <div class="flex justify-beetwen items-center gap-4 md:gap-0 mt-[32px] md:mt-[56px] xl:mt-[48px]">
        <h2 class="md:w-[87%] lg:w-[90%] xl:w-[92%] 2xl:w-[94%] font-rubik text-[16px] font-[600] text-[#424259]">{{$t('translation.main.cliyent.six')}} <span class="text-[#2588AF]">100+</span> {{$t('translation.main.cliyent.seven')}}</h2>
        <div class="md:w-[10%] lg:w-[10%] xl:w-[8%] 2xl:w-[6%] flex items-center gap-[20px]">
            <div class=" top-0 -left-4 h-full items-center">
                <button @click="prevSlide" role="button" class="prev px-2 py-2 rounded-full text-[#2588AF] border border-[#2588AF] hover:bg-[#2588AF] hover:text-white group" aria-label="prev"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5 group-active:-translate-x-2 transition-all duration-200 ease-linear">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M15.75 19.5L8.25 12l7.5-7.5" />
                    </svg>
    
                </button>
            </div>
            <div class=" top-0 -right-4 h-full items-center">
                <button @click="nextSlide" role="button" class="next px-2 py-2 rounded-full text-[#2588AF] border border-[#2588AF] hover:bg-[#2588AF] hover:text-white group" aria-label="next"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5 group-active:translate-x-2 transition-all duration-200 ease-linear">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M8.25 4.5l7.5 7.5-7.5 7.5" />
                    </svg>
                </button>
            </div>
        </div>
       </div>
    </div>
</template>

<script setup>
    import { ref, computed, onMounted, onBeforeUnmount } from 'vue';

    const slidesContainer = ref(null); // Ref to the slides container element

    const slideWidth = computed(() => {
    if (!slidesContainer.value) return 0;
    return slidesContainer.value.querySelector('.slide').clientWidth;
    });

    const scrollLeft = (amount) => {
    if (!slidesContainer.value) return;
    slidesContainer.value.scrollLeft += amount;
    };

    const nextSlide = () => scrollLeft(slideWidth.value);
    const prevSlide = () => scrollLeft(-slideWidth.value);

    const onSlideChange = (event) => {
    // Handle slide change event (optional)
    };

    onMounted(() => {
        slidesContainer.value.addEventListener('scroll', onSlideChange);
    });

    onBeforeUnmount(() => {
        slidesContainer.value.removeEventListener('scroll', onSlideChange);
    });
</script>


<style lang="scss" scoped>
    .slides-container {
        -ms-overflow-style: none; /* Internet Explorer 10+ */
        scrollbar-width: none; /* Firefox */
    }
    .slides-container::-webkit-scrollbar {
        display: none; /* Safari and Chrome */
    }

</style>