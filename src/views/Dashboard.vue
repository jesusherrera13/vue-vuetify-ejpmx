<template>
    <PageComponent title="Dasboard">
        <template v-slot:content>
    
            <v-row>
                <v-col
                    cols="12"
                    sm="2"
                >
                    <v-sheet
                        rounded="lg"
                        min-height="268"
                    >

                        <v-card
                            class="mx-auto"
                            max-width="344"
                        >
                            <v-card-text>
                                <div>FINAL</div>
                                <div class="text-caption">Liga de Baseball Clase Abierta</div>
                                <v-row align="center" no-gutters>
                                    <v-col
                                        cols="3"
                                    >
                                        <v-avatar
                                            size="28px"
                                        >
                                            <v-img
                                                alt="Avatar"
                                                src="https://avatars0.githubusercontent.com/u/9064066?v=4&s=460"
                                            ></v-img>
                                        </v-avatar>
                                    </v-col>
                                    <v-col cols="6" class="text-h6">
                                        Texas
                                    </v-col>
                                    <v-col cols="3" class="text-right text-h6">
                                        7
                                    </v-col>
                                </v-row>

                                <v-row align="center" no-gutters>
                                    <v-col
                                        cols="3"
                                    >
                                        <v-avatar
                                            size="28px"
                                        >
                                            <v-img
                                                alt="Avatar"
                                                src="https://cdn.vuetifyjs.com/images/lists/4.jpg"
                                            ></v-img>
                                        </v-avatar>
                                    </v-col>
                                    <v-col cols="6" class="text-h6">
                                        Tampa Bay
                                    </v-col>
                                    <v-col cols="3" class="text-right text-h6">
                                        1
                                    </v-col>
                                </v-row>
                                <!-- <p>adjective</p>
                                <div class="text--primary">
                                    well meaning and kindly.<br>
                                    "a benevolent smile"
                                </div> -->
                            </v-card-text>
                            <!-- <v-card-actions>
                                <v-btn
                                    variant="text"
                                    color="deep-purple-accent-4"
                                >
                                    Learn More
                                </v-btn>
                            </v-card-actions> -->
                        </v-card>


                    </v-sheet>
                </v-col>
    
                <v-col
                    cols="12"
                    sm="6"
                >
                    <CardComponent
                        src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
                        title="What's next after blockbuster Scherzer trade?"
                        subtitle="1,000 miles of wonder"
                        text="With Max Scherzer headed to the Rangers per MLB.com's Mark Feinsand, what does it mean for Justin Verlander's future? Does Texas have more trades up its sleeve? Let's break it all down."
                    >
                    </CardComponent>
                </v-col>
    
                <v-col
                    cols="12"
                    sm="3"
                >
                    <v-sheet
                        rounded="lg"
                        min-height="268"
                    >
                        <v-list
                            :items="items"
                            item-props
                            lines="three"
                        >
                            <template v-slot:subtitle="{ subtitle }">
                                <div v-html="subtitle"></div>
                            </template>
                        </v-list>
                    </v-sheet>
                </v-col>
            </v-row>
        </template>
    </PageComponent>
</template>

<script setup>
import PageComponent from '../components/PageComponent.vue';
import CardComponent from '../components/CardComponent.vue';

const items = [
        { type: 'subheader', title: 'NOTICIAS' },
        {
          prependAvatar: 'https://cdn.vuetifyjs.com/images/lists/1.jpg',
          title: 'Brunch this weekend?',
          subtitle: `<span class="text-primary">Ali Connors</span> &mdash; I'll be in your neighborhood doing errands this weekend. Do you want to hang out?`,
        },
        { type: 'divider', inset: true },
        {
          prependAvatar: 'https://cdn.vuetifyjs.com/images/lists/2.jpg',
          title: 'Summer BBQ',
          subtitle: `<span class="text-primary">to Alex, Scott, Jennifer</span> &mdash; Wish I could come, but I'm out of town this weekend.`,
        },
        { type: 'divider', inset: true },
        {
          prependAvatar: 'https://cdn.vuetifyjs.com/images/lists/3.jpg',
          title: 'Oui oui',
          subtitle: '<span class="text-primary">Sandra Adams</span> &mdash; Do you have Paris recommendations? Have you ever been?',
        },
        { type: 'divider', inset: true },
        {
          prependAvatar: 'https://cdn.vuetifyjs.com/images/lists/4.jpg',
          title: 'Birthday gift',
          subtitle: '<span class="text-primary">Trevor Hansen</span> &mdash; Have any ideas about what we should get Heidi for her birthday?',
        },
        { type: 'divider', inset: true },
        {
          prependAvatar: 'https://cdn.vuetifyjs.com/images/lists/5.jpg',
          title: 'Recipe to try',
          subtitle: '<span class="text-primary">Britta Holt</span> &mdash; We should eat this: Grate, Squash, Corn, and tomatillo Tacos.',
        },
      ];

</script>