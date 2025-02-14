<template>
  <div class="body__container">
    <messenger-input @send ="addMessage"/>
    <messenger-message  
    v-for="m in messageArray" 
    :key="m.id"     
    :message="m"/>
  </div>
 

</template>

<script>
import MessengerInput from './MessengerInput.vue'
import MessengerMessage from './MessengerMessage.vue'
export default {
  name: 'MessengerBody',
  components: {
    MessengerInput,
    MessengerMessage
  },
  data() {
    return {
      messageArray: [],

    }
  },
  methods: {
    addMessage(sendedMessage) {
      this.messageArray.push(
        {
          id: new Date().getTime(),
          message: sendedMessage,
        }
      )
      console.log(this.messageArray)
    },
  }
}
</script>
<style scoped>
 .body__container {
    padding: 50px;
}

</style>