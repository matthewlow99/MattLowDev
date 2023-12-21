<script>
    import LanguageIcon from "../images/LanguageIcon.svelte";
    import {fade} from "svelte/transition";
    import 'bootstrap/dist/css/bootstrap.min.css';
    import 'bootstrap/dist/js/bootstrap.bundle.min.js';

    export let project;
    let imageIndex = 0;
    let showText = false;

    function showMoreText(){
        showText = !showText;
    }
    function nextImageButtonPress(){
        imageIndex = imageIndex + 1;
    }

</script>

<div class="d-flex flex-row flex-wrap justify-content-evenly align-items-center container" style="gap: 20px" id="projectEntry_{project.id}" transition:fade>

    <div class="d-flex flex-column align-content-center justify-content-evenly">
        <h1 class="text-light mb-5">{project.title}</h1>
        <span class="row justify-content-center mb-5">
            {#each (project?.languageIcons || []) as icon}
                    <LanguageIcon class="col" imageName={icon} />
                {/each}
        </span>


            {#if !showText}
                <p class="text-light text-center">{project?.summary}</p>

            {:else}
                {#each project.text as t}
                    <p class="text-light">{t}</p>
                {/each}
            {/if}


        <div class="d-flex flex-row w-100 justify-content-evenly">
            {#if project.productLink}<a class="linkButton" href={project.productLink} target="_blank">View Project</a>{/if}
            {#if project.projectLink}<a class="linkButton " href={project.projectLink} target="_blank">View GitHub</a>{/if}
            <a class="linkButton" on:click={showMoreText}>{showText ? 'Show Less' : 'Show More'}</a>
        </div>

    </div>

    {#if !showText}
    <div class="d-flex flex-column align-items-center justify-content-center">
        <img src={project.images[imageIndex % project?.images?.length]} class="imageMask" />
        <p class="imageMask nextImage" on:click={nextImageButtonPress}>Next Image</p>
    </div>
    {/if}
</div>


<!--<div class="fullScreen" id="projectEntry_{project.id}" >-->

<!--    <div class="projectContainer" transition:fade>-->

<!--        <div class="infoColumn">-->
<!--            <h1>{project.title}</h1>-->
<!--            <span style="display: flex;flex-direction: row; gap: 20px">-->
<!--                {#each (project?.languageIcons || []) as icon}-->
<!--                        <LanguageIcon imageName={icon}/>-->
<!--                    {/each}-->
<!--            </span>-->

<!--            <div class="descriptionText">-->
<!--                {#if !showText}-->
<!--                    <p >{project?.summary}</p>-->

<!--                    {:else}-->
<!--                    {#each project.text as t}-->
<!--                        <p>{t}</p>-->
<!--                    {/each}-->
<!--                {/if}-->
<!--            </div>-->

<!--            <span style="width: 60%; display: flex; justify-content: space-between">-->
<!--                {#if project.productLink}<a class="linkButton" href={project.productLink} target="_blank">View Project</a>{/if}-->
<!--                {#if project.projectLink}<a class="linkButton" href={project.projectLink} target="_blank">View GitHub</a>{/if}-->
<!--                <a class="linkButton" on:click={showMoreText}>{showText ? 'Show Less' : 'Show More'}</a>-->
<!--            </span>-->

<!--        </div>-->

<!--        {#if !showText}-->
<!--            <div>-->
<!--                <div style="height: 500px; width: 930px">-->
<!--                    <img src={project.images[imageIndex % project?.images?.length]} class="imageMask"/>-->
<!--                </div>-->
<!--                <p class="imageMask nextImage" on:click={nextImageButtonPress}>Next Image</p>-->
<!--            </div>-->
<!--        {/if}-->


<!--    </div>-->
<!--</div>-->


<style>
    .fullScreen {
        display: flex;
        /*gap: 20px;*/
        width: 100%;
        min-height: 100vh;
    }
    .imageMask {
        /*mask-image: radial-gradient(rgba(0, 0, 0, 1), rgba(0, 0, 0, 1), rgba(0, 0, 0, 0));*/
        border-radius: 10px;
        /*max-width: 50%;*/
        max-height: 100%;
        min-width: 300px;
        width: 35vw;
    }
    .descriptionText {
        width: 80%;
    }
    .infoColumn {
        display: flex;
        /*height: 100%;*/
        flex: 1;
        flex-direction: column;
        justify-content: space-between;
        align-items: center;
        gap: 20px;
    }
    .linkButton {
        background: linear-gradient(to right, rgba(10, 10, 130, .6), rgba(130, 0, 130, .6));
        color: white;
        /*height: fit-content;*/
        text-decoration: none;
        padding: 10px 20px;
        font-weight: 600;
        /*font-size: 16pt;*/
        border: 1px solid black;
        border-radius: 5%;
    }
    .linkButton:hover {
        color: white;
        cursor: pointer;
        background: linear-gradient(to right, rgba(20, 20, 255, .3), rgba(255, 0, 255, .3));
    }
    .nextImage{user-select: none;}
    .nextImage:hover {
        /*color: black;*/
        cursor: pointer;
    }
    .projectContainer {
        /*opacity: 0;*/
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        width: 80%;
        margin: auto;
        transition: opacity;
    }

    .projectContainer h1 {
        color: white;
        font-size: 45pt;
        text-align: center;
        margin: 0;
    }
    .projectContainer p {
        color: white;
        font-size: 16pt;
        text-align: center;
    }
</style>