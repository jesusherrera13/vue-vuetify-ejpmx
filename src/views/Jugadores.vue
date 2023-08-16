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
                  xxx
                  </v-sheet>
              </v-col>
  
              <v-col
                  cols="12"
                  sm="6"
              >
                <v-sheet elevation="3" rounded class="pa-4">
                  <h1>Jugadores</h1>
                </v-sheet>
                 <!--  <CardComponent
                      src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
                      title="What's next after blockbuster Scherzer trade?"
                      subtitle="1,000 miles of wonder"
                      text="With Max Scherzer headed to the Rangers per MLB.com's Mark Feinsand, what does it mean for Justin Verlander's future? Does Texas have more trades up its sleeve? Let's break it all down."
                  >
                  </CardComponent> -->
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