<template>
    <div class="row vh-100">
        <div class="col-md-5 color-background d-flex flex-column justify-content-center align-items-center">
            <h1 class="text-light text-center">Sistema <br><span>Acadêmico</span></h1>
           <div class="mt-5">
                <img class="img" src="../../assets/img/logo.png" alt="">
           </div>
        </div>

        <div class="text-font col-md-7 d-flex justify-content-center align-items-center">
            <div class="w-50 ">
                <h1 class="text-center mb-5">Login</h1>
                <form @submit.prevent="submitForm()" class="d-flex flex-column mt-5">
                    <label for="">Email</label>
                    <input v-model="email" class="my-2 mb-2 border-bottom border-0 no-focus-outline" type="email" name="email">
                    <label for="">Senha</label>
                    <input v-model="password" class="my-2 mb-3 border-bottom border-0 no-focus-outline" type="password" name="password">
                    <button type="submit" class="my-3 p-2 color-background text-light border-0 rounded"> Entrar</button>
                </form>
            </div>
        </div>
    </div>    
</template>
<script>
export default {
    data() {
        return {
            email: '',
            password: ''
        }
    },
    methods: {
        submitForm(){
            console.log("Email: ", this.email)
            console.log("Senha: ", this.password)
        }
    }

}
</script>
<style>
 .color-background{
    background: #5F81F9;
 }
 .text-font{
    color: #5F81F9;
 }
 .img{
    width: 160px;
    height: 160px;
 }
 .no-focus-outline:focus {
    outline: none;
  }
</style>