<template>
  <div>
    <h1>Event Create, {{ user.name }}, {{ catLength }}</h1>
    <p>this event created by {{ user.name }}</p>
    <ul>
      <li v-for="cat in categories" :key="cat">{{ cat }}</li>
    </ul>
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  computed: {
    catLength() {
      return this.$store.getters.catLength
    },
    ...mapState(['user', 'categories'])
  }
}
</script>

<style></style>
