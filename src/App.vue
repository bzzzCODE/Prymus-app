<template>
  <div>
    <div>
      <h1>Participants list</h1>
      <ul v-if="participants.length > 0">
        <li> :key="participant" v-for="participant in participants">{{ participants }}</li>
      </ul>
    </div>

    <h3>New participant</h3>
    <form @submit.prevent="addNewParticipant()">
      <label>Firstname</label>
      <input type="text">
      <br>
      <label>Lastname</label>
      <input type="text">
      <button>Add new participant</button>
    </form>
  </div>
</template>

<script>
  export default {
    data() {
      return {participants: []};
    },
    methods: {
      addNewParticipant() {
        this.participants.push(Firstname)
      }
    }
  };
</script>

