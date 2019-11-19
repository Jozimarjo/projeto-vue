<template>
    <v-app id="inspire">

        <v-content>
            <v-container>
                <v-btn color="success" @click="btn = !btn">teste
                    <v-icon>mdi-plus</v-icon>
                </v-btn>
            </v-container>
        </v-content>
        <v-content>
            <v-container>
                <h1>Motorola</h1>
                <v-card>
                    <v-img class="white--text align-end"  contain
                           src="https://images-na.ssl-images-amazon.com/images/G/32/br-marketing-coop/Setembro/Motorola/Banner_Amazon_1500x375_BrandPage_Desk._CB436436140_.png">
                        <v-card-title>Top 10 Celulares motorolas</v-card-title>
                    </v-img>

                </v-card>
            </v-container>
            <HelloWorld v-if="btn"/>
            <CardHorizontal v-if="btn"/>
            <CardProduto v-if="!btn"/>
        </v-content>
        <!--      // cortana ficar por baixo-->
        <v-navigation-drawer disable-resize-watcher v-model="drawer" clipped app>
            <v-list dense>
                <template v-for="item in items">
                    <v-row v-if="item.heading" :key="item.heading" align="center">
                        <v-col cols="6">
                            <v-subheader v-if="item.heading">
                                {{ item.heading }}
                            </v-subheader>
                        </v-col>
                        <v-col cols="6" class="text-center">
                            <a href="#!" class="body-2 black--text">EDIT</a>
                        </v-col>
                    </v-row>
                    <v-list-group v-else-if="item.children" :key="item.text" v-model="item.model"
                                  :prepend-icon="item.model ? item.icon : item['icon-alt']" append-icon="">
                        <template v-slot:activator>
                            <v-list-item>
                                <v-list-item-content>
                                    <v-list-item-title>
                                        {{ item.text }}
                                    </v-list-item-title>
                                </v-list-item-content>
                            </v-list-item>
                        </template>

                        <v-list-item v-for="(child, i) in item.children" :key="i" link>
                            <v-list-item-action v-if="child.icon">
                                <v-icon>{{ child.icon }}</v-icon>
                            </v-list-item-action>
                            <v-list-item-content>
                                <v-list-item-title>
                                    {{ child.text }}
                                </v-list-item-title>
                            </v-list-item-content>
                        </v-list-item>
                    </v-list-group>
                    <v-list-item v-else :key="item.text" link>
                        <v-list-item-action>
                            <v-icon>{{ item.icon }}</v-icon>
                        </v-list-item-action>
                        <v-list-item-content>
                            <v-list-item-title>
                                {{ item.text }}
                            </v-list-item-title>
                        </v-list-item-content>
                    </v-list-item>
                </template>
            </v-list>
        </v-navigation-drawer>


        <!--      // toolbar em toda tela-->
        <v-app-bar clipped-left app color="blue darken-3" dark>
            <v-toolbar-title style="width: 300px" class="ml-0 pl-4">
                <v-app-bar-nav-icon @click.stop="drawer = !drawer"/>
                <span >Nome app</span>
            </v-toolbar-title>
            <v-text-field flat solo-inverted hide-details prepend-inner-icon="mdi-magnify" label="Search"
                          class="hidden-sm-and-down"/>
            <v-spacer/>
            <v-btn icon>
                <v-icon>mdi-apps</v-icon>
            </v-btn>
            <v-btn icon>
                <v-icon>mdi-bell</v-icon>
            </v-btn>
            <v-btn icon large>
                <v-avatar size="32px" item>
                    <v-img src="https://cdn.vuetifyjs.com/images/logos/logo.svg" alt="Vuetify"/>
                </v-avatar>
            </v-btn>
        </v-app-bar>
        <v-content>
            <v-container class="fill-height" fluid>

            </v-container>
        </v-content>
        <v-btn bottom color="pink" dar fab fixed right @click="dialog = !dialog">
            <v-icon>mdi-plus</v-icon>
        </v-btn>
        <v-dialog v-model="dialog" width="800px">
            <v-card>
                <v-card-title class="grey darken-2">
                    Create contact
                </v-card-title>
                <v-container>
                    <v-row>
                        <v-col class="align-center justify-space-between" cols="12"
                        >
                            <v-row align="center">
                                <v-avatar size="40px" class="mr-4">
                                    <img src="//ssl.gstatic.com/s2/oz/images/sge/grey_silhouette.png" alt="">
                                </v-avatar>
                                <v-text-field placeholder="Name"/>
                            </v-row>
                        </v-col>
                        <v-col cols="6">
                            <v-text-field prepend-icon="business" placeholder="Company"/>
                        </v-col>
                        <v-col cols="6">
                            <v-text-field placeholder="Job title"/>
                        </v-col>
                        <v-col cols="12">
                            <v-text-field prepend-icon="mail" placeholder="Email"/>
                        </v-col>
                        <v-col cols="12">
                            <v-text-field type="tel" prepend-icon="phone" placeholder="(000) 000 - 000"
                            />
                        </v-col>
                        <v-col cols="12">
                            <v-text-field prepend-icon="notes" placeholder="Notes"/>
                        </v-col>
                    </v-row>
                </v-container>
                <v-card-actions>
                    <v-btn text color="primary">More</v-btn>
                    <v-spacer/>
                    <v-btn text color="primary" @click="dialog = false">Cancel</v-btn>
                    <v-btn text @click="dialog = false">Save</v-btn>
                </v-card-actions>
            </v-card>
        </v-dialog>
    </v-app>

</template>

<script>
    /* eslint-disable */
    import HelloWorld from './components/HelloWorld';
    import CardHorizontal from './components/card-horizontal'
    import CardProduto from './components/card-produto'
    //
    export default {
        name: 'App',

        components: {
            HelloWorld,
            CardHorizontal,
            CardProduto
        },

        data: () => ({
            dialog: false,
            drawer: null,
            btn: false,
            pessoa: [
                {nome: 'Jozimar', idade: 23, cpf: '123456789'},
                {nome: 'kevin', idade: 23, cpf: '123456789'},
                {nome: 'deyveson', idade: 23, cpf: '123456789'},
                {nome: 'lulu', idade: 23, cpf: '123456789'}],
            teste: {},
            pos: '',
            nome: '',
            items: [
                {icon: 'mdi-contacts', text: 'Contacts'},
                {icon: 'mdi-history', text: 'Frequently contacted'},
                {icon: 'mdi-content-copy', text: 'Duplicates'},
                {
                    icon: 'mdi-chevron-up',
                    'icon-alt': 'mdi-chevron-down',
                    text: 'Labels',
                    model: true,
                    children: [
                        {icon: 'mdi-plus', text: 'Create label'},
                    ],
                },
                {
                    icon: 'mdi-chevron-up',
                    'icon-alt': 'mdi-chevron-down',
                    text: 'More',
                    model: false,
                    children: [
                        {text: 'Import'},
                        {text: 'Export'},
                        {text: 'Print'},
                        {text: 'Undo changes'},
                        {text: 'Other contacts'},
                    ],
                },
                {icon: 'mdi-settings', text: 'Settings'},
                {icon: 'mdi-message', text: 'Send feedback'},
                {icon: 'mdi-help-circle', text: 'Help'},
                {icon: 'mdi-cellphone-link', text: 'App downloads'},
                {icon: 'mdi-keyboard', text: 'Go to the old version'},
            ],
            //
        }),
        methods: {
            edit(item) {

                console.log(item)
                const index = this.pessoa.findIndex(value => value.nome === item.nome)
                console.log('A posicao e ', this.pessoa[index].nome)
                this.teste = this.pessoa[index];

                // this.teste = this.pessoa[0];


            },
            teste1() {
                console.log(this.nome)

                let x = {nome: '', idade: '21', cpf: '12212121'}
                x.nome = this.nome;
                this.pessoa.push(x);
            }
        }
    };
</script>
