<script>
    import RoboHash from "../lib/RoboHash.svelte";
    let robot1;
    let robot2;
</script>

<h1>Welcome to RoboHash-SVG-Svelte</h1>
<p>
<RoboHash bind:this={robot1} width={500} height={500} string="VCpL+ttOxnunjiptuA5AB+JjFYcAFOMOVPuVLt/HE2Q="/>

<button on:click={() => robot1.start()}>start</button>
</p>
<p>
<RoboHash bind:this={robot2} width={500} height={500} string="TPHp5v7aZbfmHFL5w/nEM9nToyATqyvsyt/JDPR2dkk="/>

<button on:click={() => robot2.start()}>start</button>
</p>