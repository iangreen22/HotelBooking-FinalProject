<script>
import Navbar from './components/Navbar.vue';
import RoomList from './components/RoomList.vue';
import Form from './components/Form.vue';


export default {
  components: {
    Navbar, RoomList, Form
  },
  data() {
    return {
      rooms: [
        {
          id: 1,
          name: 'Deluxe Suite',
          type: 'Suite',
          price: 195,
          capacity: 4,
          image: '/images/suite.jpg',
          amenities: ['WiFi', 'Aircon', 'TV', 'Breakfast']
        },
        {
          id: 2,
          name: 'Deluxe Room',
          type: 'Deluxe',
          price: 125,
          capacity: 2,
          image: '/images/deluxe.jpg',
          amenities: ['WiFi', 'Aircon', 'TV']
        },
        {
          id: 3,
          name: 'Standard Room',
          type: 'Standard',
          price: 95,
          capacity: 2,
          image: '/images/standard.jpg',
          amenities: ['WiFi', 'Aircon']
        },
        {
          id: 4,
          name: 'Family Suite',
          type: 'Suite',
          price: 220,
          capacity: 5,
          image: '/images/family.jpg',
          amenities: ['WiFi', 'Aircon', 'TV', 'Breakfast']
        },
        {
          id: 5,
          name: 'Twin Room',
          type: 'Standard',
          price: 110,
          capacity: 2,
          image: '/images/twin.jpg',
          amenities: ['WiFi', 'TV']
        },
        {
          id: 6,
          name: 'Executive Room',
          type: 'Deluxe',
          price: 165,
          capacity: 3,
          image: '/images/executive.jpg',
          amenities: ['WiFi', 'Aircon', 'TV', 'Mini Bar']
        }
      ],
        currentPage: 'home',
    }
  },
  methods: {
    section(page){
      this.currentPage = page;

    }
  }
}


</script>

<template>
  <Navbar @goTo="section" />
  <RoomList :roomArray="rooms"  />
  <Form />
</template>
