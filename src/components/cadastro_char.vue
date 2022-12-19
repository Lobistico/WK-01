<template>
    <v-select :items="items" label="Solo field" solo></v-select>
</template>

<script>
export default {
    name: "cadastro_char",

    data() {
        return {
            items: ["Humano", "Demônio"],
        };
    },
};
</script>
