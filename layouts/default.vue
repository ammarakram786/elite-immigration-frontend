<template>
    <div class="main-section relative font-nunito text-sm font-normal antialiased">

        <!--  BEGIN MAIN CONTAINER  -->
        <div class="relative">
            <!-- screen loader -->
            <div v-show="store.isShowMainLoader"
                class="screen_loader animate__animated fixed inset-0 z-[60] grid place-content-center bg-[#fafafa] dark:bg-[#060818]">
                <svg width="64" height="64" viewBox="0 0 135 135" xmlns="http://www.w3.org/2000/svg" fill="#4361ee">
                    <path
                        d="M67.447 58c5.523 0 10-4.477 10-10s-4.477-10-10-10-10 4.477-10 10 4.477 10 10 10zm9.448 9.447c0 5.523 4.477 10 10 10 5.522 0 10-4.477 10-10s-4.478-10-10-10c-5.523 0-10 4.477-10 10zm-9.448 9.448c-5.523 0-10 4.477-10 10 0 5.522 4.477 10 10 10s10-4.478 10-10c0-5.523-4.477-10-10-10zM58 67.447c0-5.523-4.477-10-10-10s-10 4.477-10 10 4.477 10 10 10 10-4.477 10-10z">
                        <animateTransform attributeName="transform" type="rotate" from="0 67 67" to="-360 67 67"
                            dur="2.5s" repeatCount="indefinite" />
                    </path>
                    <path
                        d="M28.19 40.31c6.627 0 12-5.374 12-12 0-6.628-5.373-12-12-12-6.628 0-12 5.372-12 12 0 6.626 5.372 12 12 12zm30.72-19.825c4.686 4.687 12.284 4.687 16.97 0 4.686-4.686 4.686-12.284 0-16.97-4.686-4.687-12.284-4.687-16.97 0-4.687 4.686-4.687 12.284 0 16.97zm35.74 7.705c0 6.627 5.37 12 12 12 6.626 0 12-5.373 12-12 0-6.628-5.374-12-12-12-6.63 0-12 5.372-12 12zm19.822 30.72c-4.686 4.686-4.686 12.284 0 16.97 4.687 4.686 12.285 4.686 16.97 0 4.687-4.686 4.687-12.284 0-16.97-4.685-4.687-12.283-4.687-16.97 0zm-7.704 35.74c-6.627 0-12 5.37-12 12 0 6.626 5.373 12 12 12s12-5.374 12-12c0-6.63-5.373-12-12-12zm-30.72 19.822c-4.686-4.686-12.284-4.686-16.97 0-4.686 4.687-4.686 12.285 0 16.97 4.686 4.687 12.284 4.687 16.97 0 4.687-4.685 4.687-12.283 0-16.97zm-35.74-7.704c0-6.627-5.372-12-12-12-6.626 0-12 5.373-12 12s5.374 12 12 12c6.628 0 12-5.373 12-12zm-19.823-30.72c4.687-4.686 4.687-12.284 0-16.97-4.686-4.686-12.284-4.686-16.97 0-4.687 4.686-4.687 12.284 0 16.97 4.686 4.687 12.284 4.687 16.97 0z">
                        <animateTransform attributeName="transform" type="rotate" from="0 67 67" to="360 67 67" dur="8s"
                            repeatCount="indefinite" />
                    </path>
                </svg>
            </div>
            <div class="main-container min-h-screen text-black dark:text-white-dark navbar-sticky">

                <div class="main-content flex min-h-screen flex-col">
                    <!--  BEGIN TOP NAVBAR  -->
                    <landing-header />
                    <!--  END TOP NAVBAR  -->

                    <!--  BEGIN CONTENT AREA  -->
                    <div class="animation p-6">
                        <NuxtPage />
                    </div>
                    <!--  END CONTENT AREA  -->

                    <!-- BEGIN FOOTER -->
                    <landing-footer />
                    <!-- END FOOTER -->
                </div>
            </div>
        </div>
    </div>
</template>
<script setup lang="ts">
import { ref, onMounted } from 'vue';
import appSetting from '@/app-setting';
import { useAppStore } from '@/stores/index';
const store = useAppStore();
const showTopButton = ref(false);
const { setLocale } = useI18n();
onMounted(() => {
    // set default settings
    // appSetting.init(setLocale);

    window.onscroll = () => {
        if (document.body.scrollTop > 50 || document.documentElement.scrollTop > 50) {
            showTopButton.value = true;
        } else {
            showTopButton.value = false;
        }
    };

    const eleanimation: any = document.querySelector('.animation');
    eleanimation.addEventListener('animationend', function () {
        appSetting.changeAnimation('remove');
    });
    store.toggleMainLoader();
});
</script>
