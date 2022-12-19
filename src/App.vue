<template>
    <v-app>
        <v-app-bar app color="gray">
            <div class="d-flex align-center">
                <v-img
                    alt="Vuetify Logo"
                    class="shrink mr-2"
                    contain
                    src="../src/assets/kmts_rpg.png"
                    transition="scale-transition"
                    width="60"
                />
            </div>
            <div class="text-center">
                <v-menu offset-y>
                    <template v-slot:activator="{ on, attrs }">
                        <v-btn color="alert" dark v-bind="attrs" v-on="on">
                            MENU
                        </v-btn>
                    </template>
                    <v-list>
                        <v-list-item
                            v-for="(item, index) in items"
                            :key="index"
                        >
                            <v-list-item-title>{{
                                item.title
                            }}</v-list-item-title>
                        </v-list-item>
                    </v-list>
                </v-menu>
            </div>

            <v-spacer style="text-align: center">
                <!-- <a href="../">INICIO</a> | <a href="../load">HISTORIA</a> |
                <a href="../about">EVENTOS</a> | <a href="../load">REGRAS</a> |
                <a href="../load">PERSONAGENS</a> |
                <a href="../load">CADASTRO</a> | <a href="../load">FICHA</a> |
                <a href="../load">NERF_AOKYN</a> -->
            </v-spacer>

            <v-btn href="https://discord.gg/BKHe7SHU4k" target="_blank" text>
                <v-img
                    alt="Vuetify Logo"
                    class="shrink mr-2"
                    contain
                    src="../src/assets/discordia.png"
                    transition="scale-transition"
                    width="50"
                />
                <span class="mr-2">Discord</span>
                <v-icon>mdi-open-in-new</v-icon>
            </v-btn>
        </v-app-bar>

        <v-main>
            <router-view />
        </v-main>
        <v-footer dark padless>
            <v-card class="flex" flat tile>
                <v-card-title class="black">
                    <v-spacer>berekatban</v-spacer>

                    <v-btn
                        v-for="icon in icons"
                        :key="icon"
                        class="mx-4"
                        dark
                        icon
                    >
                        <v-icon size="24px">
                            {{ icon }}
                        </v-icon>
                    </v-btn>
                </v-card-title>

                <v-card-text class="py-2 white--text text-center">
                    <strong> L.R. Silva Carvalho</strong> -
                    {{ new Date().getFullYear() }}
                </v-card-text>
            </v-card>
        </v-footer>
    </v-app>
</template>

<script>
export default {
    name: "App",

    data: () => ({
        items: [
            { title: "INICIO" },
            { title: "HISTÓRIA" },
            { title: "REGRAS" },
            { title: "PERSONAGENS" },
            { title: "CADASTRO" },
            { title: "FICHA" },
            { title: "#NERF_AOKYN" },
        ],
    }),
};
</script>
