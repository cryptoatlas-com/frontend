<template>
  <div id="globeContainer"></div>
</template>

<script lang="ts">
import { onMounted, ref } from 'vue';
import * as THREE from 'three';
import { Globe } from 'three-globe';

export default {
  name: 'GlobeComponent',
  setup() {
    const globeContainer = ref(null);

    onMounted(() => {
      const globe = new Globe()
        .globeImageUrl('//unpkg.com/three-globe/example/img/earth-night.jpg')
        .bumpImageUrl('//unpkg.com/three-globe/example/img/earth-topology.png')
        .labelsData([{ lat: 0, lng: 0, name: '0,0' }]);

      const renderer = new THREE.WebGLRenderer();
      const scene = new THREE.Scene();
      scene.add(globe);
      const camera = new THREE.PerspectiveCamera();
      camera.position.z = 300;

      const animate = () => {
        requestAnimationFrame(animate);
        renderer.render(scene, camera);
      };
      animate();

      globeContainer.value.appendChild(renderer.domElement);
    });

    return { globeContainer };
  },
};
</script>

<style scoped>
#globeContainer {
  width: 100%;
  height: 100vh;
}
</style>
