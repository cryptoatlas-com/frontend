<template>
  <q-page class="row items-center justify-evenly">
    <globe></globe>
  </q-page>
</template>

<script lang="ts">
import Globe from 'components/Globe.vue';
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'GlobePage',
  components: { Globe },
});
</script>
