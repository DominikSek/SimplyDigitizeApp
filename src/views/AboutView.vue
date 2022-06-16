<template>
  <h1>{{$route.params.id}}</h1>
  <Renderer resize="window" orbit-ctrl>
    <Camera :position="{ z: 10 }" />
    <Scene background="#fff">
      <AmbientLight :intensity="0.5" />
      <PointLight :position="{ x: -450, y: 350, z: 100 }" intensity="4"/>
      <GltfModel src="/models/scene.gltf"/>
    </Scene>
  </Renderer>
</template>

<script>
  import { AmbientLight, GltfModel, Camera, LambertMaterial, PointLight, Renderer, Scene ,Box} from 'troisjs';
  export default {
    components: { AmbientLight, GltfModel, Camera, LambertMaterial, PointLight, Renderer, Scene,Box},
  };
</script>