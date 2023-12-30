<template>
    <header>
        <div class="container mx-auto h-[70px] lg:h-[90px] flex justify-between items-center xl:px-4 2xl:px-0">
            <div class="w-1/3 lg:w-1/5 xl:w-1/3">
                <img src="../../assets/images/mebelLogo.svg" alt="LOGO" class="w-[60px] lg:w-[100px]">
            </div>
            <div class="hidden lg:flex items-center gap-6 font-[700] xl:text-[18px] font-mont">
                <router-link to="#" class="hover:bg-gray-300 px-2 xl:px-2 py-1 rounded-lg">{{$t('translation.navbar.one')}}</router-link>
                <router-link to="#" class="hover:bg-gray-300 px-2 xl:px-2 py-1 rounded-lg">{{$t('translation.navbar.two')}}</router-link>
                <router-link to="#" class="hover:bg-gray-300 px-2 xl:px-2 py-1 rounded-lg">{{$t('translation.navbar.three')}}</router-link>
                <router-link to="#" class="hover:bg-gray-300 px-2 xl:px-2 py-1 rounded-lg">{{$t('translation.navbar.four')}}</router-link>
                <router-link to="#" class="hover:bg-gray-300  px-2 xl:px-2 py-1 rounded-lg">{{$t('translation.navbar.five')}}</router-link>
                <select id="countries" @change="changeLanguage" class=" bg-gray-300 px-2 py-1 border-none text-md rounded-lg ml-[50px] font-mont">
                    <option  class="hidden" value="til" :selected="selectedLanguage === 'uz'">{{$t('translation.language')}}</option>
                    <option value="uz">O'zbekcha</option>
                    <option value="ru">Русский</option>
                    <option value="en">English</option>
                </select>
            </div>
            <div class="w-[50%] md:w-[25%] flex lg:hidden justify-end items-center gap-3 text-black px-2">
                <button id="dropdownDefaultButton" data-dropdown-toggle="dropdown" class="xl:hidden">
                    <i class='bx bx-menu text-[32px]'></i>
                </button>
                    <!-- Dropdown menu -->
                <div id="dropdown" class="z-10 hidden bg-gray-300 divide-y divide-gray-100 rounded-lg shadow w-22 dark:bg-gray-700">
                    <ul class="py-2 text-[16px] font-Satoshi dark:text-gray-200" aria-labelledby="dropdownDefaultButton">
                        <li>
                            <router-link to="/" class="block px-4 py-2">{{$t('translation.navbar.one')}}</router-link>
                        </li>
                        <li>
                            <router-link to="/services" class="block px-4 py-2">{{$t('translation.navbar.two')}}</router-link>
                        </li>
                        <li>
                            <router-link to="/portfolio" class="block px-4 py-2">{{$t('translation.navbar.three')}}</router-link>
                        </li>
                        <li>
                            <router-link to="/about" class="block px-4 py-2">{{$t('translation.navbar.four')}}</router-link>
                        </li>
                        <li>
                            <p class="block px-4 py-2">{{ $t('translation.navbar.five') }}</p>
                        </li>
                    </ul>
                </div>
                <select id="countries" @change="changeLanguage" class="bg-gray-300 px-2 py-1 border-none text-md rounded-lg">
                    <option  class="hidden" value="til" :selected="selectedLanguage === 'uz'">{{$t('translation.language')}}</option>
                    <option value="uz">O'zbekcha</option>
                    <option value="ru">Русский</option>
                    <option value="en">English</option>
                </select>
            </div>
        </div>
    </header>
</template>

<script setup>
    import { initFlowbite } from 'flowbite'
    import { ref, onMounted } from "vue";
    import { useRouter } from "vue-router";
    import { useI18n } from 'vue-i18n';
    const {t} = useI18n({useScope: 'global'})

    function changeLanguage(event) {
        const selectedLanguage = event.target.value;
        console.log(selectedLanguage);
        localStorage.setItem("lang", selectedLanguage)
        window.location.reload()
    }
</script>

<style lang="scss" scoped>

</style>