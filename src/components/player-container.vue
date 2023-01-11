<template>
    <article>
        <div class="image-container">
            <img src="" alt="portada_image">
        </div>
        <div class="player-container">
            <div class="plyr__controls">
                <img class="player-button" src="../assets/bx-play.svg" alt="">
                <div class="progres-bar">
                    <img src="../assets/bxs-circle.svg" alt="">
                </div>
                <p>00:00</p>
                <p>/</p>
                <p>02:30</p>   
                <img src="../assets/bx-volume-full.svg" alt="">
                <div class="progres-bar">
                    <img src="../assets/bxs-circle.svg" alt="">
                </div>
                <audio src="" preload></audio>
            </div> 
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
    margin: 2rem 15%;
}
.image-container {
    position: relative;
    top: 60px;
    width: 70%;
    height: 80%;
    background-color: var(--fresh-red);
    border-radius: 4px;
    padding: 8%;
    overflow: hidden;
}

.player-container {
    background-color: var(--just-black);
    width: 70vw;
    height: 15vh;
    border-radius: 4px;
}

.plyr__controls {
    padding: 0 3%;
    padding-top: 7rem;
    width: auto;
    height: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.plyr__controls > p {
    color: var(--just-white);
}

.progres-bar {
    display: flex;
    flex-direction: column;
    background-color: transparent;
    width: 1rem;
}

audio {
    position: relative;
    right: 40px;
    top: 80px;
    transform: scale(0.7);
}

@media screen and (min-width: 760px) {

    article {
        width: 71%;
        margin: 2rem 25%;
    }

    .player-container {
        width: 50vw;
    }

    .plyr__controls {
        justify-content: space-evenly;
    }

    .plyr__controls img {
        transform: scale(1.2);
    }

    .plyr__controls > p {
        font-size: large;
    }

}

@media screen and (min-width: 1024px) {

    article {
        width: 40%;
        margin: 2rem 35%;
    }

    .player-container {
        width: 28vw;
        height: 20vh;
    }

}

</style>