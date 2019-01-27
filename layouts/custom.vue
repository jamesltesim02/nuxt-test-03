<template>
  <v-app>
    <v-toolbar>
      <v-toolbar-side-icon />
      <v-toolbar-title>Title</v-toolbar-title>
      <v-spacer />
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn
          v-for="(item, i) in items"
          :key="i"
          flat
          :to="item.to"
          router
          exact
        >
          {{ item.title }}
        </v-btn>
      </v-toolbar-items>
    </v-toolbar>
    <nuxt />
  </v-app>
</template>
<script>
export default {
  data() {
    return {
      items: [
        {
          icon: 'apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'bubble_chart',
          title: 'Inspire',
          to: '/inspire'
        },
        {
          icon: 'bubble_chart',
          title: 'custome',
          to: '/cuspage'
        }
      ]
    }
  }
}
</script>
