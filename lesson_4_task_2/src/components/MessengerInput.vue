<template>
    <div class="input__container">
        <input type="text" v-model.trim="message">
        <button @click="onSend" class="input__button">Send</button>
    </div>
</template>

<script>
    export default {
        name: 'MessengerInput',
        data() {
            return {
                message: null
            }
        },
        methods: {
            onSend() {
                this.$emit('send', this.message)
                this.onClear()
            },
            onClear() {
                this.message = null
            }
        }
    }
</script>
<style scoped>
 .input__container {
       display: flex;
       gap: 20px;
       
    }
    .input__container input {
        padding: 10px;
        width: 100px;
        font-size: 24px;
        border-radius: 10px;
    }
    .input__button {
        font-size: 24px;
        border-radius: 10px;
    }
    
</style>