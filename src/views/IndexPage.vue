<template>
    <div class="min-h-screen max-w-screen bg-slate-950 ">
        <nav class="transparent text-white border-gray-200 dark:bg-white-900">
            <div class="max-w-full flex flex-wrap items-center justify-between md:py-4 px-2 py-2 ">
                <div class="flex items-center space-x-3 rtl:space-x-reverse">

                </div>
                <button @click="navStore.showNavar" data-collapse-toggle="navbar-default" type="button"
                    class="inline-flex items-center p-2 w-10 h-10 justify-center text-sm text-gray-500 rounded-lg md:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600"
                    aria-controls="navbar-default" aria-expanded="false">
                    <span class="sr-only">Open main menu</span>
                    <svg class="w-5 h-5" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none"
                        viewBox="0 0 17 14">
                        <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                            d="M1 1h15M1 7h15M1 13h15" />
                    </svg>
                </button>
                <div class="hidden w-full md:block md:w-auto" id="navbar-default" :class="{ visible: navStore.navarState }">
                    <ul
                        class="font-medium flex flex-col p-4 md:p-0 mt-4 bg-transparent bg-gray-50 md:flex-row md:space-x-8 rtl:space-x-reverse">
                        <li>
                            <a href="#home"
                                class="block py-2 px-3 text-white md:bg-transparent md:p-0 rounded hover:bg-gray-500 hover:text-slate-950">Home</a>
                        </li>
                        <li>
                            <a href="#services"
                                class="block py-2 px-3 text-white md:bg-transparent md:p-0 rounded hover:bg-gray-500 hover:text-slate-950">Services</a>
                        </li>
                        <li>
                            <a href="#works"
                                class="block py-2 px-3 text-white md:bg-transparent md:p-0 rounded hover:bg-gray-500 hover:text-slate-950">Works</a>
                        </li>
                    </ul>
                </div>
            </div>
        </nav>
        <!-- Main content -->
        <div class="flex-grow flex flex-col max-h-full max-w-full">
            <!-- First section -->
            <div class="flex-1 grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 text-white max-h-full max-w-full" id="home">
                <!-- Image in the background -->
                <div class="relative flex items-center justify-center">
                    <div class="absolute inset-0 bg-blue-500 custom-radius mx-4 md:mx-32"></div>
                    <img style="border-radius: 100px;" src="../assets/about.jpg" class="md:h-96 h-80 w-87 z-10 relative"
                        alt="Foreground Image">
                </div>



                <div>
                    <h1 class="font-mono text-blue-500 text-[70px] font-bold">
                        Franklin
                    </h1>
                    <h1 class="text-[25px] font-bold  inline font-mono">
                        <span class="animate-glow-orange font-mono">I'm a professional illustrator from Cordova !</span>
                    </h1>

                    <p class="mt-4 font-mono">
                        <br>Motivated and detail-oriented college student with
                        strong communication and analytical skills, eager to
                        gain practical experience and contribute to the growth
                        of the company. Excited to learn from experienced
                        professionals and committed to taking on new
                        challenges to develop my skills.
                        <br><br>Passionate and resourceful individual with a proven track record of generating and implementing innovative ideas across various domains. Seeking opportunities to contribute creative solutions and drive positive change in a dynamic and collaborative environment.<br>

                    </p>
                </div>
            </div>
            <!--Second section -->
            <div class="flex items-center justify-center md:mt-20 bg-slate-900 lg:mt-0 mt-4 rounded-lg" id="services">
                <div class="grid grid-cols-1 md:grid-cols-4 lg:grid-cols-4 h-full w-full text-white">
                    <div class="h-full w-full border-1 border-r">
                        <h1 class="pl-4 pt-4 text-[25px] font-mono">About Me</h1>
                        <div class="row">
                            <div class="col-lg-6">
                                <ul>
                                    <li><i class="bi bi-rounded-right"></i> <strong>Birthday:</strong> November 13, 2000
                                    </li>
                                    <li><i class="bi bi-rounded-right"></i>
                                        <strong>Website:</strong>https://www.facebook.com/pepkinfrank</li>
                                    <li><i class="bi bi-rounded-right"></i> <strong>Phone:</strong> 09665765122</li>
                                    <li><i class="bi bi-rounded-right"></i> <strong>City:</strong> City : Cebu City</li>
                                </ul>
                            </div>
                            <div class="col-lg-6">
                                <ul>
                                    <li><i class="bi bi-rounded-right"></i> <strong>Age:</strong>20</li>
                                    <li><i class="bi bi-rounded-right"></i> <strong>Degree:</strong> Master</li>
                                    <li><i class="bi bi-rounded-right"></i> <strong>PhEmailone:</strong> email@example.com
                                    </li>
                                    <li><i class="bi bi-rounded-right"></i> <strong>Freelance:</strong> Available</li>
                                </ul>
                            </div>
                        </div>

                    </div>
                    <div class="h-full w-full">
                        <div class="flex items-center ml-4">
                            <img src="../assets/basket.png" class="h-8 w-8 bg-white mt-2 rounded-2xl text-white">
                            <h1 class="pl-4 pt-4 text-[25px] font-mono">Skill</h1>
                        </div>
                        <div class="row skills-content">

                            <div class="col-lg-6">

                                <div class="progress">
                                    <span class="skill">HTML <i class="val">100%</i></span>
                                    <div class="progress-bar-wrap">
                                        <div class="progress-bar" role="progressbar" aria-valuenow="100" aria-valuemin="0"
                                            aria-valuemax="100"></div>
                                    </div>
                                </div>

                                <div class="progress">
                                    <span class="skill">CSS <i class="val">90%</i></span>
                                    <div class="progress-bar-wrap">
                                        <div class="progress-bar" role="progressbar" aria-valuenow="90" aria-valuemin="0"
                                            aria-valuemax="100"></div>
                                    </div>
                                </div>

                                <div class="progress">
                                    <span class="skill">JavaScript <i class="val">75%</i></span>
                                    <div class="progress-bar-wrap">
                                        <div class="progress-bar" role="progressbar" aria-valuenow="75" aria-valuemin="0"
                                            aria-valuemax="100"></div>
                                    </div>
                                </div>

                            </div>

                            <div class="col-lg-6">

                                <div class="progress">
                                    <span class="skill">PHP <i class="val">80%</i></span>
                                    <div class="progress-bar-wrap">
                                        <div class="progress-bar" role="progressbar" aria-valuenow="80" aria-valuemin="0"
                                            aria-valuemax="100"></div>
                                    </div>
                                </div>

                                <div class="progress">
                                    <span class="skill">WordPress/CMS <i class="val">90%</i></span>
                                    <div class="progress-bar-wrap">
                                        <div class="progress-bar" role="progressbar" aria-valuenow="90" aria-valuemin="0"
                                            aria-valuemax="100"></div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                </div>
            </div>
            <!--Third section -->
            <div class="flex items-center justify-center mt-10 md:mx-10" id="works">
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 h-full w-full text-white">
                    <div class="h-full w-full">
                        <h1 class="pl-4 pt-4 text-[25px] font-mono">WORKS</h1>
                        <p class="text-left pl-4 pt-2">
                            Work encompasses the efforts and activities individuals undertake to achieve goals,
                            contribute to progress, and generate value in various domains, whether personal, professional,
                            or societal.
                        </p>
                    </div>
                    <div class="h-full w-full">
                        <div class="flex items-center justify-center md:ml-4">
                            <img src="../assets/settings.png" class="h-8 w-8 bg-white mt-2 rounded-2xl text-white">
                            <h1 class="pl-4 pt-4 text-[25px] font-mono">Projects</h1>
                        </div>
                        <div class="flex flex-col">
                            <div class="grid grid-cols-2 md:grid-cols-2 lg:grid-cols-2 gap-x-1">
                                <!--first image-->
                                <router-link to="/todo">
                                    <div class="h-full w-full text-center">
                                        <h3>Todo App</h3>
                                        <img src="../assets/task.png" class="mx-auto w-40 h-40">
                                    </div>
                                </router-link>
                                <!--second image-->
                                <router-link to="/dictionary">
                                    <div class="h-full w-full text-center">
                                        <h3>Crazy Dictionary</h3>
                                        <img src="../assets/book.png" class="mx-auto w-40 h-40">
                                    </div>
                                </router-link>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <footer class="bg-transparent dark:bg-gray-900 mt-10 md:border-t-0 border-t-2">
            <div class="w-full max-w-screen md:py-8 text-center mt-4">
                <div class="sm:flex sm:items-center sm:justify-between">

                </div>
                <hr class="my-6 border-gray-200 sm:mx-auto dark:border-gray-700 lg:my-8" />
                <span class="block text-sm text-white sm:text-center dark:text-gray-400">© 2023-2024 <a href="#"
                        class="hover:underline">Franklin</a>. All Rights Reserved.</span>
            </div>
        </footer>
    </div>
</template>
<script setup>
import { useNavarStore } from '@/stores/';

const navStore = useNavarStore();
</script>
<style scoped>
.visible {
    display: block !important;
}

@keyframes glow-orange {
    0% {
        text-shadow: 0 0 5px cyan, 0 0 10px cyan, 0 0 15px cyan;
    }

    50% {
        text-shadow: 0 0 10px cyan, 0 0 20px cyan, 0 0 30px cyan;
    }

    100% {
        text-shadow: 0 0 15px cyan, 0 0 30px cyan, 0 0 40px cyan;
    }
}

.animate-glow-orange {
    animation: glow-orange 1.5s ease-in-out infinite;
}

.custom-radius {
    border-radius: 71% 29% 56% 44% / 74% 82% 18% 26%;
}</style>