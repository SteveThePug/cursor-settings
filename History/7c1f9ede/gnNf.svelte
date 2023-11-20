<script lang="ts">
import { onMount } from 'svelte';
import * as THREE from 'three';
export let width;
export let height;

onMount(() => {
const canvas = document.getElementById('myCanvas') as HTMLElement;
const renderer = new THREE.WebGLRenderer({ canvas: canvas, alpha: true, powerPreference: "low-power", preserveDrawingBuffer: true, antialias: false })
const width = canvas.clientWidth;
const height = canvas.clientHeight;
const  aspectRatio =  width / height;

//Create a scene
const scene = new THREE.Scene()
//Create a camera
const camera = new THREE.PerspectiveCamera(75, aspectRatio, 0.1, 1000)
camera.position.set(1, 2, 1)
camera.lookAt(0,0,0)
scene.add(camera)
//Create some lights
const light = new THREE.PointLight(0xff00ff, 1000, 1000)
light.position.set(-1, -1, -1);
scene.add(light);
const light2 = new THREE.PointLight(0xff0000, 1000, 1000)
light2.position.set(1, 1, 1);
scene.add(light2);
//Create a box
const boxGeometry = new THREE.BoxGeometry(1, 1, 1);
const boxMaterial = new THREE.MeshPhongMaterial({ color: 0x00ff00 });
const boxMesh = new THREE.Mesh(boxGeometry, boxMaterial);
boxMesh.position.set(0, 0, 0);
scene.add(boxMesh);

let time = 0

function updateCamera() {
    camera.aspect = aspectRatio
    camera.updateProjectionMatrix()
}

function updateRenderer() {
    renderer.setSize(width, height)
    renderer.render(scene, camera)
}

function loop() {
    time += 0.001
    boxMesh.rotateX(time);

    updateRenderer()
    updateCamera()
    requestAnimationFrame(loop);
}

loop()
});


</script>

<three>
    <canvas id="myCanvas"></canvas>
</three>

<style>
canvas {
    width: 100%;
    height: 100%;
}
three {
   display: flex; 
   flex: 1;
}
</style>