<template>
<v-container>
    <v-row dense>
        <v-col v-for="(category, i) in categories" :key="i" cols="3">
            <v-hover v-slot:default="{ hover }">
                <v-card dark max-width="200" class="mx-auto">
                    <v-img :src="category.Bannersrc">
                        <v-expand-transition>
                            <div v-if="hover" class="d-flex transition-fast-in-fast-out amber darken-2 v-card--reveal display-0 white--text" style="height: 100%;" v-text="category.name">

                            </div>
                        </v-expand-transition>

                    </v-img>
                </v-card>
            </v-hover>

        </v-col>
    </v-row>
    <User />
</v-container>
</template>

<script>
export default {
    data: () => {
        return {
            current: {},
            index: 0,
            categories: [{

                    Bannersrc: require('../assets/cat/wicca.jpg'),
                    name: "Wicca/Pagan"
                },

                {

                    Bannersrc: require('../assets/cat/candumb.jpg'),
                    name: "Candomblé/Umbanda"
                },
                {

                    Bannersrc: require('../assets/cat/herm.jpg'),
                    name: "Hermetismo"
                },
                {

                    Bannersrc: require('../assets/cat/alq.jpg'),
                    name: "Alquimia"
                },
                {

                    Bannersrc: require('../assets/cat/anc.jpg'),
                    name: "Conhecimento Ancestral"
                },
                {

                    Bannersrc: require('../assets/cat/asa.jpg'),
                    name: "Asatrú / Odinismo"
                },
                {

                    Bannersrc: require('../assets/cat/ast.jpg'),
                    name: "Viagem Astral"
                },
                {

                    Bannersrc: require('../assets/cat/egi.jpg'),
                    name: "Magia Egípcia"
                },
                {

                    Bannersrc: require('../assets/cat/elem.jpg'),
                    name: "Magia Elemental"
                },
                {

                    Bannersrc: require('../assets/cat/evo.jpg'),
                    name: "Evocação"
                },
                {

                    Bannersrc: require('../assets/cat/taro.jpg'),
                    name: "Tarot"
                },
                {

                    Bannersrc: require('../assets/cat/astro.jpg'),
                    name: "Astrologia"
                },

            ],

        }
    },
    components: {
        //
    },

}
</script>

<style>
.v-card--reveal {
    align-items: center;
    bottom: 0;
    justify-content: center;
    opacity: .5;
    position: absolute;
    width: 100%;
}
</style>
