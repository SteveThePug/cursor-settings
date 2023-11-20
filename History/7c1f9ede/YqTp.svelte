<script lang="ts">
import { onMount } from 'svelte';
import * as THREE from 'three';

onMount(() => {
const canvas = document.getElementById('myCanvas') as HTMLElement;
const renderer = new THREE.WebGLRenderer({ canvas });

const scene = new THREE.Scene()

const width = canvas.clientWidth;
const height = canvas.clientHeight;
const  aspectRatio =  width / height;
const camera = new THREE.PerspectiveCamera(75, aspectRatio, 0.1, 1000)
camera.position.set(0, 0, 3)
scene.add(camera)

const light = new THREE.PointLight(0xff00ff, 1000, 1000)
light.position.set(-1, -1, -1);
scene.add(light);


const light2 = new THREE.PointLight(0xff0000, 1000, 1000)
light2.position.set(1, 1, 1);
scene.add(light2);

const updateCamera() {
    camera.aspect = aspectRatio
    camera.updateProjectionMatrix()
}

function updateRenderer() {
    renderer.setSize(width.value, height.value)
    renderer.render(scene, camera)
}



});


</script>

<selection>
    <canvas id="myCanvas"></canvas>
</selection>

<style>
canvas {
    width: 10vw;
    height: 10vh;
}

</style>