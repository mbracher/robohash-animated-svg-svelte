<script>
    import RoboHash from "../lib/RoboHash.svelte";
    let robot;
</script>

<h1>Welcome to RoboHash-Svelte</h1>

<RoboHash bind:this={robot} width={500} height={500} string="VCpL+ttOxnunjiptuA5AB+JjFYcAFOMOVPuVLt/HE2Q="/>

<button on:click={() => robot.start()}>start</button>
