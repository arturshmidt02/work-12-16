<template>
    <section class="contact"> 
        <div class="container">
            <h2 class="title"> Contact me!</h2>

            <Message v-if="message" :message="message" />

            <form @submit.prevent="onSubmit" class="contact-form">              
                <AppInput v-model="user.name">Name: </AppInput>                
                <AppInput v-model="user.email" type="email"> Email: </AppInput>              
                <AppTextArea v-model="user.text">Text: </AppTextArea>
                <div class="controls">                  
                    <AppButton class="contactsBtn"> Submit! </AppButton>
                </div>
            </form>


        </div>
    </section>
</template>

<script>

export default {
    
    data() {
        return {
            message: null,
            user: {
                name: '',
                email: '',
                text: '',
            }
        }
    },
    methods: {
        onSubmit() {
            this.message = 'Submitted!'
            this.user.name = ''
            this.user.email = ''
            this.user.text = ''
            console.log(this.user)
        }
    }
}
</script>

<style lang="scss">
.contact {
    text-align: center;
    background-color: #110f9b;
    color: #fff;
    .title{color: #fff;}
    .contact-form{
        max-width: 600px;
        margin: 30px auto;
    }
    .controls{
        margin: 30px
    }
    .contactsBtn{
        color: #0f0f0f;
        border: 1px solid #0f0f0f;
        background-color: #ffffff;
    }
}
</style>