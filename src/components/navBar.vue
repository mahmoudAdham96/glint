<template>
  <div>
    <div id="mySidebar" class="sidebar" :style="[openSide ? {'width':'17rem'} : {'width':'0px'}]">
                  <div class="smoothscroll px-8 mt-8" :class="{animateText: openSide }">
                    <span> 
                    <a href="javascript:void(0)" class="absolute top-8 right-6 text-2xl text-white" @click="closeNav()">×</a>
                    <h3 class="my-3 text-green-600 text-left font-sans text-xs tracking-[.25em] font-bold">NAVIGATION</h3>
                    </span> 
                    <a class=" mt-12 py-2 no-underline text-left text-lg block text-white " href="#home" title="home">Home</a>
                    <a class=" py-2 no-underline text-left text-lg block text-white " href="#about" title="about">About</a>
                    <a class=" py-2 no-underline text-left text-lg block text-white " href="#services" title="services">Services</a>
                    <a class=" py-2 no-underline text-left text-lg block text-white " href="#works" title="works">Works</a>
                    <a class=" py-2 no-underline text-left text-lg block text-white " href="#clients" title="clients">Clients</a>
                    <a class=" py-2 no-underline text-left text-lg block text-white " href="#contact" title="contact">Contact</a>
                    <p class="text-left text-sm mt-12 text-gray-500 Class Properties leading-6">Perspiciatis hic praesentium nesciunt. Et neque a dolorum <a href='#0' class="text-gray-400 hover:text-gray-200" >voluptatem</a> porro iusto sequi veritatis libero enim. Iusto id suscipit veritatis neque reprehenderit.</p>

                      <ul class="flex justify-between w-36 mt-8">
                    <li >
                        <a class=" hover:text-white" href="#"><i class="fa fa-facebook"></i></a>
                    </li>
                    <li >
                        <a class=" hover:text-white" href="#"><i class="fa fa-twitter"></i></a>
                    </li>
                    <li >
                        <a class=" hover:text-white" href="#"><i class="fa fa-instagram"></i></a>
                    </li>
                    <li >
                        <a class=" hover:text-white" href="#"><i class="fa fa-behance"></i></a>
                    </li>
                    <li >
                        <a class=" hover:text-white" href="#"><i class="fa fa-dribbble"></i></a>
                    </li>
                </ul>
                  </div>  
</div>
<div id="main" :style="[!openSide ? {'marginLeft':'0px'} : '']" >
  <button class="text-sm cursor-pointer bg-black text-white fixed top-5 right-10 flex items-center pl-2 py-1" @click="openNav()" ><span class="pr-1 text-green-600 scroll-smooth hover:text-white tracking-[.30em]">MENU</span> <span class="px-2 text-3xl">☰</span> </button>  
  
</div>
  </div>
</template>

<script>
export default {
  data(){
    return {
      openSide:false,
    }
  },
   methods: {
 openNav() {
   this.openSide = !this.openSide;
  },
closeNav() {
   this.openSide = !this.openSide;
  }
  }
}
</script>