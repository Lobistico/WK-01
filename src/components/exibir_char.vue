<template>
    <v-select :items="items" label="Solo field" solo></v-select>
</template>

<script>
export default {
    name: "exibir_char",

    data() {
        return {
            items: ["rei", "Demônio"],
        };
    },
};
</script>
