<script>
  import Scene from './Scene.svelte'
  import { Canvas } from '@threlte/core'
  import { WebGPURenderer } from 'three/webgpu'
</script>

<Canvas
  createRenderer={(canvas) => {
    return new WebGPURenderer({
      canvas,
      antialias: true,
      forceWebGL: false
    })
  }}
>
  <Scene />
</Canvas>
