<template>
    <v-container>
        <v-card class="mx-auto" v-for="item in pessoa" :key="item.nome" @click="clicks(item)"
                style="">
            <div style="display: flex;flex-direction: column">
                <v-container>
                    <div style="" class="row">
                        <div class="col-4" style="min-height: 150px;">
                            <div style="width: 100%;height: 100%; display: flex; align-items: center">
                                <img style="max-width: 100%;height: 100%;" :src="img">
                            </div>
                        </div>
                        <div class="col-8 " style="min-height: 150px;">
                            <v-container>
                                <div style="display: flex;flex-direction: row width: 100%;height: 100%; display: flex;flex-wrap: wrap;max-height: 20%">
                                    <div>
                                        <p>{{item.nome}}</p>
                                    </div>
                                    <div style="display: flex;align-items: baseline;">
                                        <v-rating length="5" empty-icon="$ratingFull" half-increments hover size="18"
                                                  dense
                                                  color="yellow darken-3" background-color="grey darken-1">
                                        </v-rating>
                                        <v-card-text style="padding: 0px"> 2.373 Votos</v-card-text>
                                    </div>
                                    <div>
                                        <v-card-text style="padding: 5px"> Samsung · Galaxy · Galaxy A · Android · Tela
                                            de 6,2 polegadas · Reconhecimento facial · 13 megapixels · 4G LTE · 21 horas
                                            de
                                            conversação · 168 gramas
                                        </v-card-text>
                                    </div>
                                </div>
                            </v-container>
                        </div>
                    </div>
                </v-container>

                <v-expand-transition>
                    <div v-show="item.show">
                        <v-divider></v-divider>

                        <v-container>
                            <div class="row" style="display: flex;">

                                <div class="col-4" style="min-height: 150px;">
                                </div>

                                <div class="col-8">
                                    <div style="display: flex;flex-direction: row width: 100%;height: 100%; display: flex;flex-wrap: wrap;max-height: 20%;">

                                        <div style="display: flex;align-items: baseline;">
                                            <v-rating length="5" empty-icon="$ratingFull" half-increments hover
                                                      size="18"
                                                      dense
                                                      color="yellow darken-3" background-color="grey darken-1">
                                            </v-rating>
                                            <v-card-text style="padding: 0px"> 2.373 Votos</v-card-text>
                                        </div>

                                    </div>
                                </div>

                            </div>
                        </v-container>
                    </div>
                </v-expand-transition>
            </div>


        </v-card>
    </v-container>

</template>
<script>

    export default {
        name: "card-produto",
        data: () => ({
            accordion: false,
            popout: false,
            inset: false,
            multiple: false,
            disabled: false,
            readonly: false,
            focusable: false,
            pessoa: [
                {
                    nome: 'Smartphone, Motorola, Motorola One, XT1941-3, 64 GB, 5.9", Branco\n',
                    idade: 23,
                    cpf: '123456789',
                    img: 'https://images-na.ssl-images-amazon.com/images/I/61qdEFm7fGL._US133_.jpg',
                    show: false
                },

            ],
            img: 'data:image/jpeg;base64,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',

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

<style scoped>

</style>
