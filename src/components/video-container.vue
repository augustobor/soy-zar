<template>
    <article class="video-container">
        <img src="" alt="portada_video">
        <div class="video-info">
            <p>titlo_video: 3000</p>
            <p>metricas</p>
            <p>descripción</p>
            <button>Ver</button> 
        </div>
    </article>
</template>
<script>
export default {
    name: "videoContainer"
}
</script>
<style>
@import '../styles/config.css';

article.video-container {
    width: 70vw;
    height: auto;
    margin: 3rem 4rem;
    padding: 2%;
    border-radius: 4px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    background-color: var(--just-black);
}
article.video-container img {
    position: relative;
    right: 25px;
    top: -20px;
    width: 30vw;
    background-color: var(--fresh-red);
    border-radius: 4px;
    padding: 8%;
}

.video-info {
    margin-top: 0.6rem;
    font-size: medium;
    color: var(--just-white);
}

.video-info button {
    margin: 1rem 0rem;
    width: 100%;
    border-radius: 8px;
    font-size: small;
    background-color: var(--berry-red);
}

@media screen and (min-width: 420px) {
    
    article.video-container {
        width: 80vw;
        margin: 3rem 10%;
    }
    article.video-container img {
        width: 45vw;
    }

}

@media screen and (min-width: 760px) {

    article.video-container {
        width: 50vw;
        height: 30vh;
        margin: 3rem 25%;
        padding: 1%;
    }

    article.video-container img {
        right: 45px;
        width: 25vw;
    }

    .video-info {
        margin-top: 2rem;
        font-size: large;
    }

    .video-info button {
        margin: 3rem 0rem;
        font-size: x-large;
    }

}


@media screen and (min-width: 1024px) {

article.video-container {
    width: 30vw;
    height: auto;
    margin: 3rem 35%;
}

article.video-container img {
    width: 15vw;
    height: 40vh;
}

.video-info {
    margin-top: 5rem;
    font-size: large;
}

.video-info button {
    margin: 3rem 0rem;
    font-size: x-large;
}

}


</style>