<template>
  <q-page class="flex flex-center">
    <img alt="Quasar logo" src="~assets/quasar-logo-full.svg">
    <div>
      <q-card inline>
        <q-card-media>
          <img src="~assets/donuts.png">
        </q-card-media>
        <q-card-title>
          Cafe Basilico
          <q-rating slot="subtitle" v-model="stars" :max="5" />
          <div slot="right" class="row items-center">
            <q-icon name="place" /> 250 ft
          </div>
        </q-card-title>
        <q-card-main>
          <p>$・Italian, Cafe</p>
          <p class="text-faded">Small plates, salads & sandwiches in an intimate setting. As rosquinhas mais gostosas do mundo...</p>
        </q-card-main>
        <q-card-separator />
        <q-card-actions>
          <q-btn flat round dense icon="event" />
          <q-btn flat label="5:30PM" />
          <q-btn flat label="7:30PM" />
          <q-btn flat label="9:00PM" />
          <q-btn flat color="primary" label="Reserve" />
        </q-card-actions>
      </q-card>
    </div>
    <div>
      <q-btn
        @click="$q.notify('My message')"
        color="primary"
        label="Show a notification"
      />

      <q-btn
        @click="showNotification"
        color="primary"
        label="Show another notification"
      />
    </div>
  </q-page>
</template>

<style>
</style>

<script>
export default {
  name: 'PageIndex',
  methods: {
    showNotification() {
      this.$q.notify('Some other message')
    }
  }
}
</script>
