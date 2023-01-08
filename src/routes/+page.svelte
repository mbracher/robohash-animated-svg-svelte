<script  lang="ts">
	import Robohash from "../lib/robohash.svelte";

    let robot1: Robohash;

</script>

<h1>Welcome to Robohash-animated-svg-svelte</h1>
<p>
<Robohash bind:this={robot1} width={500} height={500} value="VCpL+ttOxnunjiptuA5AB+JjFYcAFOMOVPuVLt/HE2Q="/>

<!-- TODO: enable/disable the right button depending on the state of the animation -->
<button on:click={() => robot1.start()}>start animation</button>
<button on:click={() => robot1.stop()}>stop animation</button>
</p>

<p>
{#each Array(10) as _, i}
    <Robohash width={200} height={200} index={i}/>
{/each}
</p>
