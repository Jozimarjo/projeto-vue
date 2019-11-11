<template>
    <v-container fluid>
        <v-layout>
            <v-row>
                <v-col xs="12" sm="6" md="4" lg="3" xl="auto" v-for="item in pessoa" :key="item.nome">
                    <v-card max-width="344" class="mx-auto">
                        <v-list-item>
                            <v-list-item-avatar color="grey"></v-list-item-avatar>
                            <v-list-item-content>
                                <v-list-item-title class="headline"> {{item.nome}} Our Changing Planet
                                </v-list-item-title>
                                <v-list-item-subtitle>by Kurt Wagner</v-list-item-subtitle>
                            </v-list-item-content>
                        </v-list-item>

                        <v-img src="https://cdn.vuetifyjs.com/images/cards/mountain.jpg" height="194"></v-img>

                        <v-card-text>
                            Visit ten places on our planet that are undergoing the biggest changes today.
                        </v-card-text>

                        <v-card-actions>
                            <v-btn text color="deep-purple accent-4">
                                Read
                            </v-btn>
                            <v-btn text color="deep-purple accent-4">
                                Bookmark
                            </v-btn>
                            <v-spacer></v-spacer>
                            <v-btn icon>
                                <v-icon>mdi-heart</v-icon>
                            </v-btn>
                            <v-btn icon>
                                <v-icon>mdi-share-variant</v-icon>
                            </v-btn>
                        </v-card-actions>
                    </v-card>
                </v-col>

            </v-row>

        </v-layout>

    </v-container>

</template>
<script>
    export default {
        name: 'HelloWorld',

        props: {},
        watch: {},
        data: () => ({
            pessoa: [
                {nome: 'Jozimar', idade: 23, cpf: '123456789'},
                {nome: 'kevin', idade: 23, cpf: '123456789'},
                {nome: 'deyveson', idade: 23, cpf: '123456789'},
                {nome: 'lulu', idade: 23, cpf: '123456789'},
                {nome: 'lulu', idade: 23, cpf: '123456789'},
                {nome: 'lulu', idade: 23, cpf: '123456789'},
                {nome: 'lulu', idade: 23, cpf: '123456789'},
                {nome: 'lulu', idade: 23, cpf: '123456789'},
                {nome: 'lulu', idade: 23, cpf: '123456789'},
                {nome: 'lulu', idade: 23, cpf: '123456789'},
                {nome: 'lulu', idade: 23, cpf: '123456789'},
                {nome: 'lulu', idade: 23, cpf: '123456789'}
            ],
            teste: {},
            pos: '',
            nome: '',
            cards: [
                {title: 'Pre-fab homes', src: 'https://cdn.vuetifyjs.com/images/cards/house.jpg', flex: 12},
                {title: 'Favorite road trips', src: 'https://cdn.vuetifyjs.com/images/cards/road.jpg', flex: 6},
                {title: 'Best airlines', src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg', flex: 6},
            ],
        })
    }
</script>
