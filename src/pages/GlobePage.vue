<template>
  <q-page class="row items-center justify-evenly">
    <GlobeComponent></GlobeComponent>
  </q-page>
</template>

<script lang="ts">
import GlobeComponent from 'components/Globe.vue';
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'GlobePage',
  components: { GlobeComponent },
});
</script>
