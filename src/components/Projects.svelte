<script>
    import data from '../../public/data.json'
    import ProjectEntry from "./Projects/ProjectEntry.svelte";
    import 'bootstrap/dist/css/bootstrap.min.css';
    import 'bootstrap/dist/js/bootstrap.bundle.min.js';

    let projectID = 0;
    export let returnButtonPress;
    function headerButtonPress(newID){
        projectID = newID;
    }
</script>


<div class="navbar navbar-expand-xl">
    <div class="container-fluid nav-justified d-flex flex-row">
        <button class="navbar-toggler" data-bs-target="#nav" data-bs-toggle="collapse"> <div class="navbar-toggler-icon"/> </button>
        <div class="collapse navbar-collapse" id="nav">
            <ul class="navbar-nav flex-grow-1 justify-content-between w-100 align-content-center" >
                <li class="nav-item">
                    <p class="nav-link m-1 navItem text-light" on:click={returnButtonPress}>Matthew Low</p>
                </li>
                {#each data as project}
                    <li class="nav-item navItem" on:click={()=>{headerButtonPress(project.id)}}>
                        <p class="nav-link m-1 text-light">{project.title}</p>
                    </li>
                {/each}
            </ul>
        </div>

    </div>

</div>


<div id="projectContainer">
    {#each data as project}
        {#if project.id === projectID}
            <ProjectEntry {project}/>
        {/if}
    {/each}
</div>



<style>
    .navItem{
        padding-right: 10px;
        padding-left: 10px;
    }
    .navItem:hover{
        cursor: pointer;
    }
    .projectTitleHeaderContainer {
        color: white;
        /*display: flex;*/
        /*position: fixed;*/
        /*background-color: #000002;*/
        /*top: 0;*/
        /*left: 0;*/
        /*width: 100%;*/
        /*flex-direction: row;*/
        /*justify-content: space-evenly;*/
    }
    .returnButton:hover {
        color: white;
        cursor: pointer;
    }
    .projectTitleHeaderContainer  p {
        color: white;
    }
    .projectTitleHeaderContainer  p:hover {
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
        display: flex;
        margin-top: 10vh;
        height: max-content;
    }
    .projectContainerAnimated {
        animation-name: fadeOutAndIn;
        animation-duration: 1s;
        animation-iteration-count: 1;
    }
</style>