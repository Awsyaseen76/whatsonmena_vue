<template>
    <div>
        <v-toolbar class='lime'>
            <v-app-bar-nav-icon v-if="$vuetify.breakpoint.smAndDown" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
            <v-spacer class="hidden-md-and-up"></v-spacer>
            <v-toolbar-title class="green--text text--darken-4">{{appTitle}}</v-toolbar-title>
            <v-spacer class="hidden-sm-and-down"></v-spacer>
            <template v-if="$vuetify.breakpoint.mdAndUp">
                <v-toolbar-items  v-for="(item, index) in items" :key='index' class="green--text text--darken-4">
                    <v-tab :to="item.title" active-class="white--text">{{item.title}}</v-tab>
                </v-toolbar-items>
            </template>
        </v-toolbar>
        <v-navigation-drawer v-model="drawer" absolute temporary>
            <v-list nav>
                <v-list-item-group v-model="group" active-class="green--text text--darken-4">
                    <v-list-item  v-for='(item, index) in items' :key='index' display="block">
                        <v-list-item-content>
                            <router-link :to='item.title'>
                                <v-list-item-title class="text-center green--text text--accent-4">
                                    {{item.title}}
                                </v-list-item-title>
                            </router-link>
                        </v-list-item-content>
                    </v-list-item>
                </v-list-item-group>
            </v-list>
        </v-navigation-drawer>
    </div>
</template>




<script>
    export default {
        name: 'AppNavigation',
        data() {
            return {
                appTitle: 'WhatsonMENA',
                drawer: false,
                group: null,
                items: [
                    { title: 'home' },
                    { title: 'about' },
                    { title: 'login' },
                    { title: 'signup' }
                ]
            };
        },
        watch: {
            group(){
                this.drawer = false
            }
        }
    }
</script>

<style scoped>
    a{
        text-decoration: none;
    }
</style>