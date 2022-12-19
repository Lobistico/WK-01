<template>
    <v-container>
        <v-row class="text-center">
            <v-col cols="12">
                <v-img
                    :src="require('../assets/kmts_rpg.png')"
                    class="my-3"
                    contain
                    height="500"
                />
            </v-col>

            <v-col class="mb-4">
                <h1 class="display-2 font-weight-bold mb-3">
                    Um pouco sobre as regras
                </h1>

                <p color="red" class="subheading font-weight-regular">ess</p>
            </v-col>
        </v-row>
        <div class="overflow-hidden">
            <div class="text-center mb-8">
                <v-btn color="deep-purple" outlined @click="active = !active">
                    Personagens
                </v-btn>
            </div>

            <v-bottom-navigation
                v-model="value"
                :input-value="active"
                color="indigo"
            >
                <v-btn>
                    <span>Oden</span>

                    <v-icon>mdi-sword</v-icon>
                </v-btn>

                <v-btn>
                    <span>Oden</span>

                    <v-icon>mdi-sword</v-icon>
                </v-btn>

                <v-btn>
                    <span>Oden</span>

                    <v-icon>mdi-sword</v-icon>
                </v-btn>
            </v-bottom-navigation>
        </div>

        <v-timeline>
            <oi>
                <v-timeline-item> Entre em Contato com o Vigor</v-timeline-item>
                <v-timeline-item> oi</v-timeline-item>
            </oi>
        </v-timeline>
    </v-container>

    <!-- INICIO FOOTER -->
</template>

<script>
export default {
    name: "HelloWorld",

    data() {
        return {
            value: 1,
            active: true,
        };
    },
};
</script>
