<template>
    <div class="d-flex align-center justify-center" style="height:100vh;">
        <v-card width="500" class="pa-8  text-center">
            <h1 class="my=">Sign In page</h1>
        

            <v-form>
                <v-text-field label="Email" outlined prepend-inner-icon="mdi-email"></v-text-field>
                <v-text-field label="Password" outlined prepend-inner-icon="mdi-lock" type="password"></v-text-field>   
                <v-btn color="primary" rounded block><v-icon left>mdi-facebook</v-icon>  sign in</v-btn>
                <p class="my=5">or</p>
                <v-btn color="green" @click="signInWithGoogle()"><v-icon left>mdi-google</v-icon>Sign In with Google</v-btn>
            </v-form>

        </v-card>

    </div>
</template>

<script>
export default{
    layout: "auth",
    middleware: 'guest',
    methods: {
        signInWithGoogle(){
            this.$auth.loginWith('google')
        }
    }
}


</script>

