<script>

    let posX = Math.random().toPrecision(4) * 100;
    let posY = Math.random().toPrecision(4) * 100

    let delay = Math.random().toPrecision(2) * 5
    let duration = (Math.random().toPrecision(2) * 5) + 2

    let blur = Math.random();
</script>

<style>
    .starBody {
        position: absolute;
        background-color: white;
        width: 2px;
        height: 2px;
        border-radius: 50%;
        top: var(--posY);
        left: var(--posX);
        transition: opacity ease-in-out;
        box-shadow: 0 0 2px var(--blur) white; /* Adjust the values as needed */
    }
    @keyframes starFadeKeyframe {
        0% {
            opacity: 1; /* 100% opacity */
        }
        50% {
            opacity: 0.1; /* 50% opacity */
        }
        100% {
            opacity: 1; /* 100% opacity */
        }
    }
    .starFadeAnimation {
        animation-timing-function: linear;
        animation-name: starFadeKeyframe;
        animation-delay: var(--delay);
        animation-direction: normal;
        animation-iteration-count: infinite;
        animation-duration: var(--duration);
    }
</style>

<div class="starBody starFadeAnimation" style="--posY: {posY}%; --posX: {posX}%; --delay: {delay}s; --duration: {duration}s; --blur: {blur}px"/>