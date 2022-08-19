<template>
    <article>
        <picture>
            <img src="" alt="portada_image">
        </picture>
        <div class="player-container"> 
            <audio src="" controls></audio>
        </div>
    </article>
</template>
<script>
export default {
    name: "playerContainer"
}
</script>
<style>
@import '../styles/config.css';
article {
    width: 100%;
    margin: 2rem 4rem;
    border-radius: 4px;
}
picture {
    position: relative;
    right: 60px;
    top: 20px;
    width: 90vw;
    background-color: var(--fresh-red);
    border-radius: 4px;
    padding: 8%;
}

.player-container {
    background-color: var(--just-black);
    width: 70vw;
    height: 15vh;
    border-radius: 4px;
}

audio {
    position: relative;
    right: 40px;
    top: 80px;
    transform: scale(0.7);
}

</style>