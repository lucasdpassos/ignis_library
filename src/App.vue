<template>
<v-app>
    <v-app-bar app color="grey darken-4" dark prominent>
        <v-img src="./assets/logo.png" style="max-width:300px; margin-top:-1%">

        </v-img>
        <v-text-field class='display-0 white--text font-weight-thin subtitle-1' style="margin-left: 5%; margin-top:5%">Tecnologia à favor da sua expansão de consciência</v-text-field>
    </v-app-bar>

    <v-main>

        <Body />
    </v-main>

    <Footer />
</v-app>
</template>

<script>
import Footer from './components/Footer'
import Body from './components/Body'

export default {
    name: 'App',

    components: {
        Footer,
        Body
    },

    data: () => ({
        //
    }),
};
</script>
