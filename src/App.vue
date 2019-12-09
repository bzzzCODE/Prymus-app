<template>
  <div>
    <div>
      <h1>Participants list</h1>
      <ol v-if="participants.length > 0">
        <li :key="person" v-for="person in participants">{{person}}</li>
      </ol>
    </div>

    <h3>New participant</h3>
    <form @submit.prevent="addNewParticipant()">
      <label>Firstname</label>
      <input type="text" v-model="firstname">
      <br>
      <label>Lastname</label>
      <input type="text" v-model="lastname">
      <button>Add new participant</button>
    </form>
  </div>
</template>

<script>
  export default {
    data() {
      return {participants: [], firstname: "", lastname: ""};
    },
    methods: {
      addNewParticipant() {
        if(this.firstname.length > 0 && this.lastname.length > 0) this.participants.push(this.firstname +" "+ this.lastname),
                this.firstname="",
                this.lastname="";
      }
    }
  };
</script>

