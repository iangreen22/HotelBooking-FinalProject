<script>
import Navbar from './components/Navbar.vue';

  
  export default {
    components: {
    Navbar,
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
  </template>
