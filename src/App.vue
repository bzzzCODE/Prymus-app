<template>
  <div>
    <h1>{{title ? "Happy" : "Sad"}}</h1>
    <button @click="iAmClicked()">Click me!</button>
  </div>
</template>

<script>
  export default {
    data() {
      return {title: false}
    },
    methods: {
      iAmClicked() {
        this.title = !this.title;
      },
    }
  };
</script>
