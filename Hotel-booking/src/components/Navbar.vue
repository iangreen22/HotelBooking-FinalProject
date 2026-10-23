<script>
export default {
props:[],
emits:['goTo'],

  data() {
    return {
      
    
    }
  },

  methods: {
    menu(i){
        this.$emit('goTo', i)
    }
  }
}

</script>
<template>

    <header class="absolute inset-x-0 top-0 z-50 w-full">
        <nav class="mx-auto flex h-24 max-w-[1600px] items-center justify-between px-5 sm:px-8 lg:px-12"
            aria-label="Main navigation">
            <a href="#"
                class="group flex items-center gap-3 focus:outline-none focus-visible:ring-2 focus-visible:ring-lime-400 focus-visible:ring-offset-2 rounded-lg">
                <img src="../assets/logo.png" alt="" class="h-[80px] w-[80px]">
                
                <span class="text-xl font-black uppercase tracking-tight text-stone-950">Jib&nbsp;<span
                        class="text-lime-500">  </span>Hotel&nbsp;</span>
            </a>

            <ul class="hidden items-center gap-10 lg:flex">
                <li>
                    <a @click="menu('home')" href="#" aria-current="page"
                        class="relative text-sm font-bold uppercase tracking-[0.08em] text-stone-950 transition-colors duration-200 focus:outline-none focus-visible:ring-2 focus-visible:ring-lime-400">
                        HOME
                        <span class="absolute -bottom-1.5 left-0 h-[3px] w-full rounded-full bg-lime-400"></span>
                    </a>
                </li>
                <li>
                    <a @click="menu('about')" href="#"
                        class="text-sm font-bold uppercase tracking-[0.08em] text-stone-500 transition-colors duration-200 hover:text-stone-950 focus:outline-none focus-visible:ring-2 focus-visible:ring-lime-400">
                        ABOUT
                    </a>
                </li>
                <li>
                    <a @click="menu('services')" href="#"
                        class="text-sm font-bold uppercase tracking-[0.08em] text-stone-500 transition-colors duration-200 hover:text-stone-950 focus:outline-none focus-visible:ring-2 focus-visible:ring-lime-400">
                        SERVICES
                    </a>
                </li>
            
                <li>
                    <a @click="menu('contact')" href="#"
                        class="text-sm font-bold uppercase tracking-[0.08em] text-stone-500 transition-colors duration-200 hover:text-stone-950 focus:outline-none focus-visible:ring-2 focus-visible:ring-lime-400">
                        Contact
                    </a>
                </li>
                <li>
                    <a @click="menu('room')" href="#"
                        class="text-sm font-bold uppercase tracking-[0.08em] text-stone-500 transition-colors duration-200 hover:text-stone-950 focus:outline-none focus-visible:ring-2 focus-visible:ring-lime-400">
                        Contact
                    </a>
                </li>
            </ul>

            <div class="flex items-center gap-4">
                <a href="#"
                    class="group relative hidden items-center gap-2.5 overflow-hidden rounded-full border-2 border-stone-950 bg-stone-950 px-6 py-3 text-sm font-bold uppercase tracking-[0.06em] text-white transition-colors duration-300 hover:text-stone-950 focus:outline-none focus-visible:ring-2 focus-visible:ring-lime-400 focus-visible:ring-offset-2 lg:inline-flex">
                    <span
                        class="text-white absolute inset-0 -translate-x-full bg-lime-400 transition-transform duration-300 ease-out group-hover:translate-x-0"></span>
                    <span class="relative">My Reservation</span>
                    <svg class="relative h-4 w-4 transition-transform duration-300 group-hover:translate-x-1"
                        fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2.5">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M17 8l4 4m0 0l-4 4m4-4H3" />
                    </svg>
                </a>

                <input type="checkbox" id="agency-nav-toggle" class="peer hidden" />
                <label for="agency-nav-toggle"
                    class="relative z-[60] flex h-12 w-12 cursor-pointer flex-col items-center justify-center gap-[5px] rounded-full border-2 border-stone-950 transition-colors duration-300 peer-checked:border-white focus-within:ring-2 focus-within:ring-lime-400"
                    aria-label="Toggle menu">
                    <span
                        class="h-0.5 w-5 origin-center rounded-full bg-stone-950 transition-all duration-300 peer-checked:translate-y-[6.5px] peer-checked:rotate-45 peer-checked:bg-white"></span>
                    <span
                        class="h-0.5 w-5 rounded-full bg-stone-950 transition-all duration-200 peer-checked:opacity-0"></span>
                    <span
                        class="h-0.5 w-5 origin-center rounded-full bg-stone-950 transition-all duration-300 peer-checked:-translate-y-[6.5px] peer-checked:-rotate-45 peer-checked:bg-white"></span>
                </label>

                <div
                    class="invisible fixed inset-0 z-50 flex scale-95 flex-col justify-center bg-stone-950 px-6 opacity-0 transition-all duration-300 ease-out peer-checked:visible peer-checked:scale-100 peer-checked:opacity-100 lg:hidden">
                    <nav class="flex flex-col gap-2" aria-label="Mobile navigation">
                        <a href="#" aria-current="page"
                            class="border-b border-white/10 py-4 text-4xl font-black uppercase tracking-tight text-lime-400">Work</a>
                        <a href="#"
                            class="border-b border-white/10 py-4 text-4xl font-black uppercase tracking-tight text-white transition-colors duration-200 hover:text-lime-400">Studio</a>
                        <a href="#"
                            class="border-b border-white/10 py-4 text-4xl font-black uppercase tracking-tight text-white transition-colors duration-200 hover:text-lime-400">Services</a>
                        <a href="#"
                            class="border-b border-white/10 py-4 text-4xl font-black uppercase tracking-tight text-white transition-colors duration-200 hover:text-lime-400">Journal</a>
                        <a href="#"
                            class="py-4 text-4xl font-black uppercase tracking-tight text-white transition-colors duration-200 hover:text-lime-400">Contact</a>
                    </nav>
                    <a href="#"
                        class="mt-8 inline-flex w-fit items-center gap-2.5 rounded-full bg-lime-400 px-6 py-3.5 text-sm font-bold uppercase tracking-[0.06em] text-stone-950 transition-transform duration-200 active:scale-95">
                        Start a Project
                        <svg class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2.5">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M17 8l4 4m0 0l-4 4m4-4H3" />
                        </svg>
                    </a>
                    <div
                        class="absolute bottom-8 left-6 right-6 flex items-center justify-between border-t border-white/10 pt-6 text-xs font-medium uppercase tracking-[0.1em] text-stone-400">
                        <span>&copy; 2026 Forma Studio</span>
                        <span>Bengaluru, IN</span>
                    </div>
                </div>
            </div>
        </nav>
    </header>
</template>