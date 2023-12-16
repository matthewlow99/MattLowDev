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
        <img src="/assets/personal/selfie.jpg" class="selfieImage"/>
        <p>
            Greetings, I'm Matthew Low, a dedicated software craftsman with an insatiable thirst for knowledge and a penchant for creating transformative digital experiences.
            My venture into the tech realm commenced with an astrophysics major, a field that fueled my curiosity about the cosmos. However, the allure of programming steered me towards computer science, a decision that proved pivotal despite not completing my degree.
            A compelling tech job offer became the catalyst for my foray into the dynamic world of software development.
        </p>
        <p>
            My coding odyssey initiated in high school with Java, and I soon embraced Python during my academic pursuits.
            The flame of curiosity led me to solo game development, birthing creations like Football QB Sim and Poltergeist using Unity.
            This early experimentation nurtured my passion and laid the foundation for my journey into the software development landscape.
        </p>
        <p>
            In my quest for mastery, I opted for a web development bootcamp to grasp the basics of HTML/CSS/JS.
            However, the conventional learning path proved insufficient as my curiosity led me to forge ahead independently.
            The journey into backend technologies unfolded with experimentation in Django, PHP, and Express.
            Applications like Chess and Battleship showcased my ability to tackle complexity, prompting a shift towards more modern frameworks, specifically React.
        </p>
        <p>
            Embracing React marked a turning point. I delved into REST API design, employing Django and Express to architect robust backend systems.
            The transition from PHP to React wasn't just a shift in technology; it was a paradigm shift in user experience.
            This transformation was exemplified when I was selected to revamp a local HOA website.
            What began as a PHP and MySQL project evolved into a cutting-edge React solution, demonstrating my commitment to staying at the forefront of technology.
        </p>
        <p>
            My professional journey unfolded at an IT position where my off-the-clock coding prowess did not go unnoticed.
            Recognizing my capabilities, I was entrusted with coding a mobile app, VEA, for our in-house ticket system.
            This project involved collaboration with our backend developer to construct robust endpoints.
            The React-Native application, still in use post my departure, streamlined asset and contact management, ticket creation, and secured user sessions through a sophisticated access/refresh token mechanism.
        </p>
        <p>
            My passion for learning and adaptability fuel my ability to quickly grasp new technologies and frameworks.
            Beyond the code, I bring a holistic approach to problem-solving, understanding that technology is a means to an end, with the end being a positive impact on users and businesses alike.
            If you're seeking a developer who combines technical expertise with a relentless pursuit of excellence, I'd love to explore opportunities to contribute to your projects.
        </p>
        <div style="display: flex; flex-direction: row; justify-content: space-evenly; align-items: center; flex: 1">
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