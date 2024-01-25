<template>
  <q-page class="row items-center justify-evenly">
    <globe-component></globe-component>
  </q-page>
</template>

<script lang="ts">
import GlobeComponent from 'components/GlobeComponent.vue';
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'GlobePage',
  components: { GlobeComponent },
});
</script>
