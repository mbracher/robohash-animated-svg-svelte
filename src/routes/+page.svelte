<script  lang="ts">
	import RobohashAnimatedSvg from "$lib/RobohashAnimatedSvg.svelte";

    let robot1: RobohashAnimatedSvg;

</script>

<h1>Welcome to Robohash-animated-svg-svelte</h1>
<p>
<RobohashAnimatedSvg bind:this={robot1} width={500} height={500} value="VCpL+ttOxnunjiptuA5AB+JjFYcAFOMOVPuVLt/HE2Q="/>

<!-- TODO: enable/disable the right button depending on the state of the animation -->
<button on:click={() => robot1.start()}>start animation</button>
<button on:click={() => robot1.stop()}>stop animation</button>
</p>

<p>
{#each Array(10) as _, i}
    <RobohashAnimatedSvg width={140} height={140} index={i}/>
{/each}
</p>
