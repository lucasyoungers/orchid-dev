<template>
  <div class="home">
    <ul id="messages"></ul>
    <div class="ui">
      <input type="text" v-model="message">
      <button v-on:click="send">Send</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "home",
  // components: {
  //   Message
  // },
  data: function() {
    return {
      message: ""
    };
  },
  methods: {
    send: function() {
      let messages = document.getElementById("messages");
      let newMessage = document.createElement("li");
      newMessage.innerHTML = this.message;
      messages.appendChild(newMessage);
      this.message = "";
    }
  }
};
</script>

<style scoped>
#messages {
  position: fixed;
  bottom: 20px;
}
.ui {
  position: fixed;
  bottom: 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
</style>