<template>

    <v-container>

        <v-card class="mx-auto teste" v-for="item in pessoa" :key="item.nome" @click="clicks()">
            <!--            <v-container>-->
            <v-row justify="space-between">
                <v-col cols="auto">
                    <v-img height="auto" width="auto" :src="item.img"></v-img>
                </v-col>
                <v-col class="text-center pl-0">
                    <v-row class="flex-column ma-0 fill-height" justify="center">
                        <!--                        <v-list-item-title class="headline"> Our Changing Planet</v-list-item-title>-->
                        <!--                        <v-list-item-subtitle>by Kurt Wagner</v-list-item-subtitle>-->
                        <v-col class="px-0">
                            <v-card-title>{{item.nome}}--SMEU PRIMEIRO TESTE</v-card-title>
                            <v-card-subtitle>por Motorola</v-card-subtitle>
                        </v-col>

                        <!--                        <v-col class="px-0">-->
                        <!--                            <v-list-item-title class="headline"> 2Our Changing Planet</v-list-item-title>-->
                        <!--                            <v-list-item-subtitle>2by Kurt Wagner</v-list-item-subtitle>-->
                        <!--                        </v-col>-->

                        <!--                        <v-col class="px-0">-->
                        <!--                            <v-btn icon>-->
                        <!--                                <v-icon>mdi-share-variant</v-icon>-->
                        <!--                            </v-btn>-->
                        <!--                        </v-col>-->
                    </v-row>
                </v-col>
            </v-row>
            <!--            </v-container>-->
        </v-card>
    </v-container>
</template>
<script>
    export default {
        name: 'CardoHorizontal',
        props: {},
        watch: {},
        data: () => ({
            pessoa: [
                {
                    nome: 'Smartphone, Motorola, Motorola One, XT1941-3, 64 GB, 5.9", Branco\n',
                    idade: 23,
                    cpf: '123456789',
                    img: 'https://images-na.ssl-images-amazon.com/images/I/61qdEFm7fGL._US133_.jpg'
                },
                {
                    nome: 'Smartphone Motorola One Action XT2013-1, 128 GB, 6.34\'\', Branco Polar',
                    idade: 23,
                    cpf: '123456789',
                    img: 'https://images-na.ssl-images-amazon.com/images/I/61qdEFm7fGL._US133_.jpg'

                },
                {
                    nome: 'Fone de Ouvido Pulse Max com Microfone, Motorola, SH004, Preto',
                    idade: 23,
                    cpf: '123456789',
                    img: 'https://images-na.ssl-images-amazon.com/images/I/61qdEFm7fGL._US133_.jpg'
                },
                {
                    nome: 'Smartphone, Motorola, Moto G6, XT1925, 64 GB, 5.7", Preto',
                    idade: 23,
                    cpf: '123456789',
                    img: 'https://images-na.ssl-images-amazon.com/images/I/61qdEFm7fGL._US133_.jpg'
                },
                {
                    nome: 'Smartphone, Motorola, G7 Power XT1955-1, 64GB, 6.2\'\', Lilás',
                    idade: 23,
                    cpf: '123456789',
                    img: 'https://images-na.ssl-images-amazon.com/images/I/61qdEFm7fGL._US133_.jpg'
                },
                {
                    nome: 'iphone X Apple Cinza Espacial, Tela de 5,8", 4G, 64 GB, Câmera de 12 MP',
                    idade: 23,
                    cpf: '123456789',
                    img: 'https://images-na.ssl-images-amazon.com/images/I/61qdEFm7fGL._US133_.jpg'
                },
                {
                    nome: 'iphone X Apple Cinza Espacial, Tela de 5,8", 4G, 256 GG, Câmera de 12 MP',
                    idade: 23,
                    cpf: '123456789', img: 'https://images-na.ssl-images-amazon.com/images/I/61qdEFm7fGL._US133_.jpg'

                },
                {
                    nome: 'Apple Iphone X Prateado 64Gb Com 5,8, Ios 11, Processador A11 64 Bits, Cã¢Mera Dupla De 12 Mp Desbloqueado',
                    idade: 23,
                    cpf: '123456789', img: 'https://images-na.ssl-images-amazon.com/images/I/61qdEFm7fGL._US133_.jpg'

                },
                {
                    nome: 'Iphone X 64gb Cinza Espacial Space Gray Tela 5.8  IOS 11 4G 12MP Apple',
                    idade: 23,
                    cpf: '123456789', img: 'https://images-na.ssl-images-amazon.com/images/I/61qdEFm7fGL._US133_.jpg'

                },
                {
                    nome: 'Smartphone Samsung Galaxy A10, 32Gb, Tela 6.2\'\', Azul, Sm-A105Mzbkzto',
                    idade: 23,
                    cpf: '123456789', img: 'https://images-na.ssl-images-amazon.com/images/I/61qdEFm7fGL._US133_.jpg'

                },
                {
                    nome: 'Smartphone, Samsung, Galaxy Note 9 SM-N9600ZKJZTO, 128 GB, 6.4\'\', Preto',
                    idade: 23,
                    cpf: '123456789', img: 'https://images-na.ssl-images-amazon.com/images/I/61qdEFm7fGL._US133_.jpg'

                },
                {
                    nome: 'Smartphone Samsung Galaxy A20, 32Gb, Tela 6.4\'\', Azul, Sm-A205Gzbjzto',
                    idade: 23,
                    cpf: '123456789', img: 'https://images-na.ssl-images-amazon.com/images/I/61qdEFm7fGL._US133_.jpg'

                }
            ],
            teste: {},
            pos: '',
            nome: '',
            cards: [
                {title: 'Pre-fab homes', src: 'https://cdn.vuetifyjs.com/images/cards/house.jpg', flex: 12},
                {title: 'Favorite road trips', src: 'https://cdn.vuetifyjs.com/images/cards/road.jpg', flex: 6},
                {title: 'Best airlines', src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg', flex: 6},
            ],
        }),
        methods: {
            clicks() {
            }
        }
    }
</script>
<style>
    .teste {
        margin-bottom: 1%;
    }
</style>
