<script>
    import {fade} from "svelte/transition";
    export let returnButtonPress;
</script>

<div style="display: flex; flex-direction: row; align-items: center" transition:fade>
    <h2 style="flex:1;" on:click={returnButtonPress} class="returnButton">{'< Return'}</h2>
    <h1 style="flex: 1; text-align: center">About Me</h1>
    <h2 style="flex: 1"/>

</div>
<div style="display: flex; flex-direction: row; justify-content: space-evenly; width: 70%; margin-right: auto; margin-left: auto; padding-bottom: 10%" transition:fade>

    <div style="display: inline; flex-direction: column; align-items: center; flex: 1;">
        <div style="display: flex; flex-direction: row; justify-content: space-evenly; margin-bottom: 100px">
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
            </div>
        </div>




        <div style="display: flex; flex-direction: row; justify-content: space-evenly; align-items: center; margin-top: '10%'">
            <img src="/assets/personal/ml_dev.jpg" class="subImages"/>
            <img src="/assets/personal/react_dev.jpg" class="subImages"/>
            <img src="/assets/personal/chess_dev.jpg" class="subImages"/>
            <img src="/assets/personal/code1.PNG" class="subImages"/>
        </div>
        <p>
            Thank you for taking the time to explore my journey. I'm eager to connect, collaborate, and embark on the next chapter of innovation together. I will begin relocation to the Dallas/Fort Worth area in the coming weeks.
        </p>
        <h1>Matthew Low</h1>
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
        margin-right: 50px;
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