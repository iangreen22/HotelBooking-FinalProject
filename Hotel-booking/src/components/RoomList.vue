<script>

export default {
props:['roomArray'],

  data() {
    return {
      
      roomType: 'All',
      guests: 1,
      maxPrice: 300,
      selectedRoom: null
    }
  },

  methods: {
    checkRoom(room) {
      if (this.roomType != 'All' && room.type != this.roomType) {
        return false
      }

      if (room.capacity < this.guests) {
        return false
      }

      if (room.price > this.maxPrice) {
        return false
      }

      return true
    },

    showRoom(room) {
      this.selectedRoom = room
    },

    closeRoom() {
      this.selectedRoom = null
    },

    bookRoom(room){
      this.$emit('bookRoom', room)
    }
  }
}
</script>

<template>
  <div class="p-6">

    <h1 class="text-3xl font-bold mb-5">
      Our Rooms
    </h1>

    <div class="flex gap-4 mb-6">

      <select v-model="roomType" class="border p-2 rounded">
        <option>All</option>
        <option>Standard</option>
        <option>Deluxe</option>
        <option>Suite</option>
      </select>

      <select v-model.number="guests" class="border p-2 rounded">
        <option :value="1">1 Guest</option>
        <option :value="2">2 Guests</option>
        <option :value="3">3 Guests</option>
        <option :value="4">4 Guests</option>
        <option :value="5">5 Guests</option>
      </select>

      <div>
        <p>Max Price: €{{ maxPrice }}</p>
        <input
          type="range"
          v-model.number="maxPrice"
          min="90"
          max="300"
          step="5"
        >
      </div>

    </div>

    <div class="grid grid-cols-3 gap-4">

      <RoomCard
        v-for="room in roomArray"
        v-show="checkRoom(room)"
        :key="room.id"
        :room="room"
        @viewRoom="showRoom"
        @bookRoom="bookRoom"
      />

    </div>

    <RoomDetailsModal
      v-if="selectedRoom"
      :room="selectedRoom"
      @close="closeRoom"
    />

  </div>
</template>