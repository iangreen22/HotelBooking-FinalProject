<script>
import Navbar from './components/Navbar.vue';
import HomeView from './components/HomeView.vue';
import About from './components/About.vue';
import Contact from './components/Contact.vue';
import Footer from './components/Footer.vue';



export default {
  components: {
    Navbar, HomeView, About, Contact, Footer,
  },
  data() {
    return {
      page: 'home',

    }
  },
  methods: {
    showHome(i) {
      this.page = i;
    },

  }

}

</script>

<template>
  <Navbar @go-home="showHome" />
  <HomeView v-if="page === 'home'" />
  <About v-if="page === 'about'" />
  <Contact v-if="page === 'contact'" />
  <Footer />
</template>
