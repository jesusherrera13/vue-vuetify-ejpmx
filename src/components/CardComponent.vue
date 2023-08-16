<template>
    <v-card
        class="mx-auto"
    >
        <v-img
            :src=src
            height="400px"
            cover
        ></v-img>

        <v-card-title>
            {{ title }}
        </v-card-title>

        <v-card-subtitle>
            {{ subtitle }}
        </v-card-subtitle>

        <div>
            <v-card-text>
                {{ text }}
            </v-card-text>
        </div>
    </v-card>
</template>

<script setup>
    const props = defineProps({
        src: String,
        title: String,
        subtitle: String,
        text: String,
    });
</script>