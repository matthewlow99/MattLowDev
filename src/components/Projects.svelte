<script>
    import data from '../../public/data.json'
    import ProjectEntry from "./Projects/ProjectEntry.svelte";

    let projectID = 0;
    export let returnButtonPress;
    function headerButtonPress(newID){
        projectID = newID;
    }
</script>

<div class="projectTitleHeaderContainer ">
    <h2 class="returnButton" on:click={returnButtonPress}>
        {'< Return'}
    </h2>
    {#each data as project}
        <p on:click={()=>{headerButtonPress(project.id)}}>{project.title}</p>
    {/each}
</div>

<div id="projectContainer">
    {#each data as project}
        {#if project.id === projectID}
            <ProjectEntry {project}/>
        {/if}
    {/each}
</div>



<style>
    .projectTitleHeaderContainer {
        display: flex;
        position: fixed;
        background-color: #000002;
        top: 0;
        left: 0;
        width: 100%;
        flex-direction: row;
        justify-content: space-evenly;
    }
    .returnButton:hover {
        color: white;
        cursor: pointer;
    }
    .projectTitleHeaderContainer > p {
        color: white;
    }
    .projectTitleHeaderContainer > p:hover {
        color: gray;
        cursor: pointer;
    }
    @keyframes fadeOutAndIn {
        0% {
            opacity: 1;
        }
        50% {
            opacity: 0;
        }
        100% {
            opacity: 1;
        }
    }
    #projectContainer {
        /*opacity: 0;*/
        transition: opacity 1s;
    }
    .projectContainerAnimated {
        animation-name: fadeOutAndIn;
        animation-duration: 1s;
        animation-iteration-count: 1;
    }
</style>