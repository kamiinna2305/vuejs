<template>
        <div class="message__container">
            <p class="message__text">
                {{ message.message }}
            </p>
            <p :class="checkColor()">{{ likes }}</p>
            <div class="icon__container">
                <img 
                @click="inc()"
                class="icon"
                src="/icons/like.svg" 
                alt="like">
                <img 
                @click="dec()"
                class="icon" 
                src="/icons/dislike.svg" 
                alt="dislike">
                
            </div>
        </div>
   
</template>

<script>
    export default {
        name: 'MessengerMessage',
        props: {
            message: {
                type: Object,
                default: () => ({}),
            },

        },
        data() {
            return {
                likes: 0
            }
        },
        methods: {
            inc() {
                this.likes++
            },
            dec() {
                this.likes--
            },
            checkColor() {
                let color
                if (this.likes < 0) { color = 'red'}
                else if (this.likes == 0) {color = 'standard'}
                else { color = 'green' }
                return color
            }

        }
    }
</script>
<style scoped>
.message__container {
        display: flex;
        gap: 30px;
        align-items: center;
        font-size: 24px;
    }
   
    .icon__container {
       display: flex;
       gap: 20px;
    }

.icon{
    width: 32px;
}

</style>