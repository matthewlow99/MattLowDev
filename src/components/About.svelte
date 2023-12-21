<script>
    import {fade} from "svelte/transition";
    export let returnButtonPress;
</script>



<div class="container-fluid">
    <h4 style="color: white;" on:click={returnButtonPress}>Return</h4>
    <div class="d-flex flex-row flex-wrap text-center justify-content-center">
        <img src="/assets/personal/selfie.jpg" class="selfieImage"/>
        <div>
            <p>
                Greetings! I'm Matthew Low, a passionate software craftsman dedicated to creating transformative digital experiences.
                My coding journey spans from Java to Python, where I explored solo game development with Unity.
                Alongside my web development expertise in Django, PHP, and Express, I've mastered Flask and implemented websockets for real-time interactions.
            </p>
            <p>
                The pivotal shift occurred with React, leading me to revamp a local HOA website and demonstrate my commitment to cutting-edge technology.
                In a professional IT role, I developed a React-Native app, integrating Flask and websockets for streamlined asset management and ticket creation.
                My adaptability and holistic problem-solving approach, combined with extensive experience in diverse technologies, make me a valuable asset for impactful projects.
                Let's explore opportunities for collaboration!
            </p>
            <p>
                Thank you for taking the time to explore my journey. I'm eager to connect, collaborate, and embark on the next chapter of innovation together. I will begin relocation to the Dallas/Fort Worth area in the coming weeks.
            </p>
            <h1>Matthew Low</h1>
        </div>
    </div>
</div>


<style>
    h1 {
        color: white;
    }
    .returnButton:hover {
        color: white;
        cursor: pointer;
    }
    .selfieImage {
        height: 500px;
        width: auto;
        float: left;
        border-radius: 20px;
        margin-top: 30px;
        /*background-color: blue;*/
        padding: 5px;
        background: linear-gradient(to right, rgba(20, 20, 255, .3), rgba(255, 0, 255, .3));
    }
    .subImages {
        width: auto;
        height: 200px;
        margin: 20px;
    }
    p {
        color: white;
        margin-top: 50px;
        margin-bottom: 50px;
        font-size: 16pt;
        text-align: left;
    }
</style>