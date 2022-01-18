<template>
  <div id="app">
    <div class="bg-image bg-cover relative bg-fixed bg-center pb-10">
            <!-- overlay -->
            <div class="bg-black absolute top-0 left-0 w-full  h-full opacity-70"></div>
            <div class="relative  text-white">
              <a class=" " href="index.html">
                  <img class="w-20 z-30 pt-8 ml-10 " src="./assets//logo.png" alt="Homepage">
              </a>
              <div class="w-11/12 m-auto pt-44 text-left">
                <p class="text-base ml-24 text-gray-500 font-bold tracking-[.20em]">WELCOME TO GLINT</p>
                <div class="flex justify-between mt-2">
                  <p class="text-4xl lg:text-6xl ml-12 md:ml-24 lg:pr-32  w-10/12 lg:w-7/12  font-semibold lg:leading-normal">
                  We are a creative group
                  of people who design
                  influential brands and
                  digital experiences.
                </p>
                <ul class="flex  md:py-4 text-xl flex-col lg:justify-between items-end  mt-8 sr-only lg:not-sr-only ">
                    <li class="border-2 my-2 border-slate-50 rounded-full w-9 h-9 text-center p-0.5">
                        <a class=" hover:text-white" href="#" data-title="facebook" ><i class="fa fa-facebook"></i></a>
                    </li>
                    <li class="border-2 my-2 border-slate-50 rounded-full w-9 h-9 text-center p-0.5">
                        <a class=" hover:text-white" href="#" data-title="twitter"><i class="fa fa-twitter"></i></a>
                    </li>
                    <li class="border-2 my-2 border-slate-50 rounded-full w-9 h-9 text-center p-0.5">
                        <a class=" hover:text-white" href="#" data-title="instagram"><i class="fa fa-instagram"></i></a>
                    </li>
                    <li class="border-2 my-2 border-slate-50 rounded-full w-9 h-9 text-center p-0.5">
                        <a class=" hover:text-white" href="#" data-title="behance"><i class="fa fa-behance"></i></a>
                    </li>
                    <li class="border-2 my-2 border-slate-50 rounded-full w-9 h-9 text-center p-0.5">
                        <a class=" hover:text-white" href="#" data-title="dribbble"><i class="fa fa-dribbble"></i></a>
                    </li>
                </ul>
                </div>
                  <div class=" ml-24 py-20">
                    <button class="border-2 w-64 md:w-52 py-3   hover:bg-white hover:text-black mr-5">START A PROJECT</button>
                    <button class="border-2 w-64 md:w-52 mt-3 sm:mt-0 py-3  hover:bg-white hover:text-black">MORE ABOUT US </button>
                  </div>
              </div>
            </div>
        </div>
    <navBar />
    <about id="about"/>
    <services/>

  </div>
</template>

<script>
import navBar from './components/navBar.vue'
import about from './components/about.vue'
import services from './components/services.vue'

export default {
  name: 'App',
  components: {
    navBar,
    about,
    services
  },
}
</script>

<style>
#app {
  font-family: "Lato", sans-serif;  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.bg-image {
  background-image: url(./assets/hero-bg.jpg);
}
.smoothscroll {
  scroll-behavior: smooth;
  margin-left:70px;
}
.animateText {
  margin-left:10px;
  transition: margin-left 1s ease-in-out !important;
}
a{
  position: relative;
}
a[data-title]:hover::after{
   content: attr(data-title);
   position: absolute;
   top: -20% ;
   right: 35px;
   color: rgb(3, 150, 3);
   font-size: 1rem;
}
/* sidebar */
.sidebar {
  height: 100%;
  width: 0;
  position: fixed;
  z-index: 1;
  top: 0;
  right: 0;
  background-color: #111;
  overflow-x: hidden;
  transition: 0.5s;
  padding-top: 8px;
}




.openbtn:hover {
  background-color: #444;
}

/* On smaller screens, where height is less than 450px, change the style of the sidenav (less padding and a smaller font size) */
@media screen and (max-height: 450px) {
  .sidebar {padding-top: 15px;}
  .sidebar a {font-size: 18px;}
}
</style>
