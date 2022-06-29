<template>
  <div class="box-content">
    <h2>Prikaz 3D modela</h2>
  </div>
  <br>
  <hr>

  <Renderer resize="window" orbit-ctrl>
    <Camera :position="{ x: -2, y: 3, z: -4.5 }" />
    <Scene background="#D7D7D7">
      <AmbientLight :intensity="0.75" />
      <PointLight :position="{ x: -450, y: 350, z: 100 }" intensity="1.25"/>
      <GltfModel :src="'/models/' + $route.params.id + '.gltf'"/>
    </Scene>
  </Renderer>
</template>

<script>
  import { AmbientLight, GltfModel, Camera, PointLight, Renderer, Scene ,Box} from 'troisjs';
  export default {
    components: { AmbientLight, GltfModel, Camera, PointLight, Renderer, Scene,Box},
  };
</script>

<style>

  h2{
    margin: 0.5rem;
  }
</style>