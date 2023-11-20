<script>
	import Three from './Three.svelte';
	import "@/utils/mathUtils"
import * as THREE from "three";
import { GLTFLoader } from "three/examples/jsm/loaders/GLTFLoader.js";
import { AsciiEffect } from "three/examples/jsm/effects/AsciiEffect";
import { TrackballControls } from "three/examples/jsm/controls/TrackballControls";
import { DRACOLoader } from "three/examples/jsm/loaders/DRACOLoader";
const setupLaptopSceneInfo = (elem) => {
    const sceneInfo = SCENE.makeSceneInfo(elem);

    gltfLoader.load("/img/laptop.glb", function (gltf) {
        const laptopMesh = gltf.scene;
        laptopMesh.scale.set(4, 4, 4);
        laptopMesh.translateY(-1);
        sceneInfo.scene.add(gltf.scene);

        const controls = new TrackballControls(sceneInfo.camera, elem);
        sceneInfo.animate = (time) => {
            laptopMesh.rotation.y = -time;
        };
    });

    return sceneInfo;

</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<Three></Three>
</section>

<style>
</style>
