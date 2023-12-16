
<script>

    export let changePageIndex;
    function viewButton(){
        document.getElementById('projectEntry_0').scrollIntoView({behavior: 'smooth'});
    }

</script>
<div class="fullScreen">
    <div>
        <p class="nameText fadeTextAnimation" style="--delay: 1s;">matthew low</p>
        <p class="nameText fadeTextAnimation" style="font-size: 3em; --delay: 3s;"> software developer</p>
    </div>

    <div style="width: fit-content">
        <p class="optionText fadeTextAnimation" style="--delay: 2s;" on:click={() => {changePageIndex(1)}}>View Portfolio</p>
        <p class="optionText fadeTextAnimation" style="--delay: 2s;" on:click={() => {changePageIndex(2)}}>About the developer</p>
        <a class="optionText fadeTextAnimation" style="--delay: 2s;" href="mailto:matthew.low99@outlook.com">Contact Me</a>
    </div>
</div>


<style>
    .nameText {
        /*color: lime;*/
        /*font-family: Cinzel;*/
        /*color: yellow;*/
        color: white;
        font-size: 5em;
        opacity: 0;
        letter-spacing: 2px;
    }
    .optionText {
        opacity: 0;
        color: lightgray;
        font-size: 2em;
        width: 100%;
        text-align: center;
        padding: 5px 10px;
        text-decoration: none;
    }
    .optionText:hover {
        color: white;
        background-color: black;
        cursor: pointer;
        font-size: 2em;
    }
    .fullScreen {
        height: 100vh;
        width: 100%;
        display: flex;
        justify-content: space-evenly;
        flex-direction: column;
        align-items: center;
        /*background-color: red;*/
    }
    @keyframes fadeTextKeyframes {
        from {
            opacity: 0;
        }
        to {
            opacity: 1;
        }
    }
    .fadeTextAnimation {
        animation-name: fadeTextKeyframes;
        animation-duration: 3s;
        animation-iteration-count: 1;
        animation-fill-mode: both;
        animation-delay: var(--delay);
    }
    .fadeText {
        opacity: 0;
        transition: opacity linear;
    }

</style>