<script  lang="ts">
    import ForkMe from "../component/ForkMe.svelte"
	import RobohashAnimatedSvg from "$lib/RobohashAnimatedSvg.svelte";

    let robot1: RobohashAnimatedSvg;
    let any_text: string;
</script>
<ForkMe repo="mbracher/robohash-animated-svg-svelte" />

<h1>Welcome to Robohash-animated-svg-svelte</h1>

<RobohashAnimatedSvg bind:this={robot1} width={500} height={500} value={any_text}/>

<p>
<!-- TODO: enable/disable the right button depending on the state of the animation -->
<button on:click={() => robot1.start()}>start animation</button>
<button on:click={() => robot1.stop()}>stop animation</button>
</p>

<p>
    <textarea bind:value={any_text} placeholder="Enter any text to change the robot"></textarea>
</p>

<p>
{#each Array(10) as _, i}
    <RobohashAnimatedSvg width={140} height={140} index={i}/>
{/each}
</p>
