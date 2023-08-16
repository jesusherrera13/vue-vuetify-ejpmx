<template>
    <v-app id="inspire">
        <v-app-bar flat>
            <v-container class="fill-height d-flex align-center">
                <v-avatar>
                    <v-img
                        src="https://cdn.vuetifyjs.com/images/john.jpg"
                        alt="John"
                    ></v-img>
                </v-avatar>

                <v-btn
                    v-for="link in links"
                    :key="link"
                    variant="text"
                    :to="link.path"
                >
                {{ link.name }}
                </v-btn>

                <v-spacer></v-spacer>

                <!-- <v-responsive max-width="260">
                    <v-text-field
                        bg-color="grey-lighten-2"
                        class="rounded-pill overflow-hidden"
                        density="compact"
                        hide-details
                        variant="solo"
                    ></v-text-field>
                </v-responsive> -->
                <v-btn icon="mdi-dots-vertical"></v-btn>

            </v-container>
        </v-app-bar>
  
      <v-main class="bg-grey-lighten-3">
        <v-container>
            <router-view :key="$route.path"></router-view>
        </v-container>
      </v-main>
    </v-app>
  </template>
  
<script setup>
    const links = [
        { name: 'Dashboard', path: '/dashboard' },
        { name: 'Jugadores', path: '/jugadores' },
    ];
</script>