<template>
  <h3>Current model: {{$route.params.id}}</h3>
  <hr>
  <Renderer resize="window" orbit-ctrl>
    <Camera :position="{ x: -2, y: 3, z: -4.5 }" />
    <Scene background="#D7D7D7">
      <AmbientLight :intensity="1.25" />
      <PointLight :position="{ x: -450, y: 350, z: 100 }" intensity="2"/>
      <GltfModel :src="'/models/' + $route.params.id + '.gltf'"/>
    </Scene>
  </Renderer>
</template>

<script>
  import { AmbientLight, GltfModel, Camera, LambertMaterial, PointLight, Renderer, Scene ,Box} from 'troisjs';
  export default {
    components: { AmbientLight, GltfModel, Camera, LambertMaterial, PointLight, Renderer, Scene,Box},
  };
</script>