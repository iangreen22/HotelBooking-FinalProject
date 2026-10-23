<script>
import HomeView from '../HomeView.vue';
import Navbar from './components/Navbar.vue';

export default {
  components: {
     Navbar, HomeView
  },
  data() {
    return {
      
    }
  },
  methods: {
   
  }
}


import RoomList from './components/RoomList.vue';

export default {
  components: {
    RoomList,
    Form,
  }
}
</script>

<template>
  <HomeView/>
  <Navbar/>

  <RoomList />
  <Form />
</template>
