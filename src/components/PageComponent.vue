<template>
     <slot name="header"></slot>
     <slot name="content"></slot>
    <!-- 
    <v-row>
        <v-col
            cols="12"
            sm="2"
        >
            <v-sheet
                rounded="lg"
                min-height="268"
            >
            </v-sheet>
        </v-col>

        <v-col
            cols="12"
            sm="7"
        >
            <v-sheet
                min-height="70vh"
                rounded="lg"
            >
            </v-sheet>
        </v-col>

        <v-col
            cols="12"
            sm="3"
        >
            <v-sheet
                rounded="lg"
                min-height="268"
            >
            </v-sheet>
        </v-col>
    </v-row> 
    -->
</template>

<script setup>
    const props = defineProps({
        title: String,
    });
</script>