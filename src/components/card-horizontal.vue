<template>

    <v-container>

        <v-card class="teste" v-for="item in pessoa" :key="item.nome" @click="clicks(item)">
            <!--            <v-container>-->
            <v-row>
                <v-col style="max-width: 172.344px;">
                    <v-img height="auto" width="auto" :src="item.img"></v-img>
                </v-col>

                <v-col style="max-width: 65%">
                    <!--                    <v-row>-->
                    <!--                        <v-col>-->
                    <v-card-title v-bind:class="item.show?'eTrue':'d-inline-block text-truncate'"
                                  style="max-width: 100%;padding: 0px">{{item.nome}}
                    </v-card-title>


                    <div style="display: flex;">
                        <v-card-subtitle style="padding: 0px" v-if="item.show">por Motorola</v-card-subtitle>

                        <v-card-text v-if="!item.show"
                                     style="color:#222;font-size: 16px!important;font-weight: bold; width: auto"> R$
                            950,79
                        </v-card-text>
                        <v-card-text v-if="!item.show"
                                     style="color:#1a0dab;font-size: 16px!important; width: auto"> CollorMaq Manaus
                        </v-card-text>

                        <v-card-text v-if="!item.show"
                                     style="padding-bottom:0;color:#129918;font-size: 15px!important; width: auto">93%
                            positivos (246)
                        </v-card-text>
                    </div>

                    <!--<v-card-subtitle>por Motorola</v-card-subtitle>-->
                    <div style="display: flex; justify-content: space-between">
                        <v-card-actions>
                            <v-rating length="5" empty-icon="$ratingFull" half-increments hover size="18" dense
                                      color="yellow darken-3" background-color="grey darken-1">
                            </v-rating>
                            <v-card-text style="padding: 5px"> 2.373 comentários:</v-card-text>

                        </v-card-actions>

                    </div>

                    <v-card-subtitle v-bind:class="item.show?'eTrue':'d-inline-block text-truncate'"
                                     style="max-width: 100%; padding: 0px"> Samsung · Galaxy · Galaxy A · Android · Tela
                        de 6,2 polegadas
                        Reconhecimento facial · 13 megapixels · 4G LTE · 21 horas de conversação · 168 gramas

                    </v-card-subtitle>

                    <v-card-subtitle v-bind:class="item.show?'eTrue':'d-inline-block text-truncate'"
                                     style="max-width: 100%; padding: 0px"> Aproveite a tela grande para assitir aos
                        seus conteúdos no
                        celular. Mergulhe nos seus
                        conteúdos e jogos favoritos com o seu Galaxy A10.
                    </v-card-subtitle>


                    <!-- style="color:#222;font-weight: bold; font-size: 20px!important;font-family: arial,sans-serif"-->
                    <v-divider v-if="item.show"></v-divider>

                    <v-expand-transition>

                        <div class="d-flex align-center" v-if="item.show">

                            <div style="width: 30%">
                                <v-card-text v-if="item.show" style="color:#222;font-size: 15px!important;"> R$ 950
                                </v-card-text>
                            </div>


                            <div class="d-flex flex-column" style="width: 70%">
                                <div class="d-flex " style="padding-bottom: 11px;">
                                    <span style="margin-right: 2%"> R$ 689,00 </span>
                                    <span style="color:#1a0dab">100 Unidades</span>
                                    <!--<span> t3</span>-->
                                </div>
                                <div class="d-flex" style="padding-bottom: 11px;">
                                    <span style="margin-right: 2%"> R$ 789,00 </span>
                                    <span style="color:#1a0dab">200 Unidades</span>
                                </div>

                                <div class="d-flex" style="padding-bottom: 11px;">
                                    <span style="margin-right: 2%"> R$ 989,00 </span>
                                    <span style="color:#1a0dab">300 Unidades</span>
                                </div>

                                <!--<v-row>-->
                                <!--<v-card-text>-->
                                <!--100 UND-->
                                <!--</v-card-text>-->
                                <!--<v-card-text>-->
                                <!--10d0 UND-->
                                <!--</v-card-text>-->
                                <!--</v-row>-->

                                <!--<v-card-text style="width: auto" class="d-inline-flex">-->
                                <!--100 UND-->
                                <!--</v-card-text>-->
                                <!--<v-card-text style="width: auto" class="d-inline-flex">-->
                                <!--R$ 1500 | 200 UND-->
                                <!--</v-card-text>-->
                                <!--<v-card-text style="width: auto" class="d-inline-flex">-->
                                <!--R$ 2000 | 300 UND-->
                                <!--</v-card-text>-->
                            </div>

                        </div>
                    </v-expand-transition>
                    <!--                        </v-col>-->

                    <!--                        <v-col class="px-0">-->
                    <!--                            <v-list-item-title class="headline"> 2Our Changing Planet</v-list-item-title>-->
                    <!--                            <v-list-item-subtitle>2by Kurt Wagner</v-list-item-subtitle>-->
                    <!--                        </v-col>-->

                    <!--                        <v-col class="px-0">-->
                    <!--                            <v-btn icon>-->
                    <!--                                <v-icon>mdi-share-variant</v-icon>-->
                    <!--                            </v-btn>-->
                    <!--                        </v-col>-->
                    <!--                    </v-row>-->
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
                    img: 'https://images-na.ssl-images-amazon.com/images/I/61qdEFm7fGL._US133_.jpg',
                    show: false
                },
                {
                    nome: 'Smartphone Motorola One Action XT2013-1, 128 GB, 6.34\'\', Branco Polar',
                    idade: 23,
                    cpf: '123456789',
                    img: 'https://images-na.ssl-images-amazon.com/images/I/61qdEFm7fGL._US133_.jpg',
                    show: false

                },
                {
                    nome: 'Fone de Ouvido Pulse Max com Microfone, Motorola, SH004, Preto',
                    idade: 23,
                    cpf: '123456789',
                    img: 'https://images-na.ssl-images-amazon.com/images/I/61qdEFm7fGL._US133_.jpg',
                    show: false
                },
                {
                    nome: 'Smartphone, Motorola, Moto G6, XT1925, 64 GB, 5.7", Preto',
                    idade: 23,
                    cpf: '123456789',
                    img: 'https://images-na.ssl-images-amazon.com/images/I/61qdEFm7fGL._US133_.jpg',
                    show: false
                },
                {
                    nome: 'Smartphone, Motorola, G7 Power XT1955-1, 64GB, 6.2\'\', Lilás',
                    idade: 23,
                    cpf: '123456789',
                    img: 'https://images-na.ssl-images-amazon.com/images/I/61qdEFm7fGL._US133_.jpg',
                    show: false
                },
                {
                    nome: 'iphone X Apple Cinza Espacial, Tela de 5,8", 4G, 64 GB, Câmera de 12 MP',
                    idade: 23,
                    cpf: '123456789',
                    img: 'https://images-na.ssl-images-amazon.com/images/I/61qdEFm7fGL._US133_.jpg',
                    show: false
                },
                {
                    nome: 'iphone X Apple Cinza Espacial, Tela de 5,8", 4G, 256 GG, Câmera de 12 MP',
                    idade: 23,
                    cpf: '123456789', img: 'https://images-na.ssl-images-amazon.com/images/I/61qdEFm7fGL._US133_.jpg',
                    show: false

                },
                {
                    nome: 'Apple Iphone X Prateado 64Gb Com 5,8, Ios 11, Processador A11 64 Bits, Cã¢Mera Dupla De 12 Mp Desbloqueado',
                    idade: 23,
                    cpf: '123456789', img: 'https://images-na.ssl-images-amazon.com/images/I/61qdEFm7fGL._US133_.jpg',
                    show: false

                },
                {
                    nome: 'Iphone X 64gb Cinza Espacial Space Gray Tela 5.8  IOS 11 4G 12MP Apple',
                    idade: 23,
                    cpf: '123456789', img: 'https://images-na.ssl-images-amazon.com/images/I/61qdEFm7fGL._US133_.jpg',
                    show: false

                },
                {
                    nome: 'Smartphone Samsung Galaxy A10, 32Gb, Tela 6.2\'\', Azul, Sm-A105Mzbkzto',
                    idade: 23,
                    cpf: '123456789', img: 'https://images-na.ssl-images-amazon.com/images/I/61qdEFm7fGL._US133_.jpg',
                    show: false

                },
                {
                    nome: 'Smartphone, Samsung, Galaxy Note 9 SM-N9600ZKJZTO, 128 GB, 6.4\'\', Preto',
                    idade: 23,
                    cpf: '123456789', img: 'https://images-na.ssl-images-amazon.com/images/I/61qdEFm7fGL._US133_.jpg',
                    show: false

                },
                {
                    nome: 'Smartphone Samsung Galaxy A20, 32Gb, Tela 6.4\'\', Azul, Sm-A205Gzbjzto',
                    idade: 23,
                    cpf: '123456789', img: 'https://images-na.ssl-images-amazon.com/images/I/61qdEFm7fGL._US133_.jpg',
                    show: false

                }
            ],
            teste: {},
            pos: '',
            nome: '',
            show: false
        }),
        methods: {
            clicks(item) {
                item.show = !item.show;
                // item.nome = "Smartphone, Motorola, Motorola One, XT1941-3, 64 GB, 5.9\", Branco"
            }
        }
    }
</script>
<style>
    .teste {
        margin-bottom: 1%;
    }


    .eTrue {
        flex-wrap: wrap
    }
</style>
