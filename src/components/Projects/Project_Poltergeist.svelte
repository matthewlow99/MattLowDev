<script>

</script>

<div class="fullScreen">

    <div class="projectContainer">
        <div class="imageColumn">

            <img src="/assets/Poltergeist/game_img1.PNG" class="imageStyle"/>
            <!--            <img src="/assets/QB_images/qb_img2.png" class="imageStyle"/>-->
            <img src="/assets/Poltergeist/game_img2.PNG" class="imageStyle"/>
        </div>
        <div style="display: flex; flex-direction: column; align-items: flex-start; justify-content: space-between">
            <h1>Football QB Simulator</h1>
            <p>
                Football QB Sim marked the inception of my Unity project endeavors in late 2020.
                Throughout its development, I independently acquired proficiency in fundamental aspects of the Unity Engine, 3D modeling, C# programming, and the exploration of diverse artificial intelligence models tailored for defensive gameplay.
                While the gameplay itself adheres to a foundational framework, it strategically accommodates player skill progression, thereby offering an engaging and evolving user experience.
            </p>
            <p>The defensive capabilities have undergone substantial enhancements throughout the development cycle.
                In the initial stages, the defensive models operated on a predetermined 'dropback' timer, transitioning uniformly into a pursuit state.
                While effective for longer plays, this approach proved vulnerable to exploitation in the case of short plays, as it lacked responsiveness to receiver cuts.
                In the current defensive model, the utilization of dropback and pursuit states persists, albeit with a refined methodology.
                The transition between these states is now triggered by a dynamic assessment of the distance between the receiver and the defender.
                Specifically, the transition initiates as soon as the distance begins to increase.
                This strategic modification not only ensures consistent performance for extended routes but also imparts a sense of equilibrium to the defensive response in the context of short routes.
            </p>
            <a href="https://www.indiedb.com/games/football-qb-sim/downloads/qb-4-0" title="Download Football QB Sim Redux - IndieDB" target="_blank"><img src="https://button.indiedb.com/download/medium/213098.png" alt="Football QB Sim Redux" /></a>
        </div>
    </div>
</div>


<style>
    .fullScreen {
        display: flex;
        min-height: 70vh;
        width: 100%;
    }
    .imageColumn {
        display: flex;
        flex-direction: column;
        gap: 20px;
    }
    .imageStyle {
        width: 400px;
    }
    .projectContainer {
        display: flex;
        flex-direction: row;
        justify-content: space-evenly;
        gap: 40px;
        height: fit-content;
        background-color: rgba(0, 0, 0, .2);
        padding: 50px 30px;
    }
    .projectContainer h1 {
        color: white;
        font-size: 40pt;
        text-align: left;
        margin: 0;
    }
    .projectContainer p {
        color: white;
        font-size: 16pt;
        text-align: left;
    }
</style>