<script>

import BackdropStar from "./BackdropStar.svelte";

let stars = new Array(230)

</script>

<div class="backdrop">
    {#each stars as star}
        <BackdropStar />
    {/each}
</div>



<style>
    .backdrop {
        position: fixed;
        top: 0;
        left: 0;
        height: 100vh;
        width: 100%;
        z-index: -1;
        padding: 0;
        pointer-events: none;
        background: linear-gradient(to bottom, #000002, #000001, #000004);
    }
</style>