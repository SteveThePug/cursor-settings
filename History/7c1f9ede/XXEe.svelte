<script lang="ts">
import { onMount } from 'svelte';
import * as THREE from 'three';

onMount(() => {
const canvas = document.getElementById('myCanvas') as HTMLElement;
const renderer = new THREE.WebGLRenderer({ canvas });

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