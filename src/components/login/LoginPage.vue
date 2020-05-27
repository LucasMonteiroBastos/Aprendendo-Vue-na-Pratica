<template>
    <v-container fluid>
        <v-row justify="center">
            <v-col
                cols="12"
                md="4"
                lg="3"
                class="text-center"
            >
                <h6 class="headline">Login</h6>
                <v-text-field
                    v-model="token"
                    label="Token"
                />

                <v-btn
                    depressed
                    dark
                    block
                    color="green"
                    @click="login"
                >
                    Login
                </v-btn>

                <v-btn
                    text
                    @click="loginAsGuest"
                >
                    Entrar como Visitante
                </v-btn>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
// AIzaSyCGh8pFT21NDZA7ZOzMd9Mg_9XdIUvluHw
    export default {
        name: 'LoginPage',
        data() {
            return {
                token: '',
            };
        },
        methods: {
            login() {
                this.$store.commit('setAuthToken', this.token);
                // alert(this.$store.state.authToken);
            },
            loginAsGuest() {

            },
        },
    };
</script>

<style scoped>
</style>
