<template>
    <div class="text-about-container">
        <p>{{ this.text }}</p>
        <hr>
    </div>
</template>

<script>
export default{
    name: 'TextAboutContainer',
    props: {
        text: String,
    }
}
</script>

<style>
@import '../styles/config.css';

.text-about-container {
    padding: 2%;
    width: auto;
    padding: 1rem 10%;
    padding-top: 4rem;
}

.text-about-container > p{
    font-size: large;
    text-align: center;
    color: var(--just-white);
}

.text-about-container > hr {
    border-style: solid;
    color: var(--berry-red);
    margin: 0 20%;
    border-width: 0.3rem;
}

@media screen and (min-width: 760px) {
    
    .text-about-container {
        width: 40%;
        padding: 1rem 30%;
        padding-top: 6rem;
    }

    .text-about-container > p { 
        font-size: xx-large;
    }

}

@media screen and (min-width: 1024px) {

    .text-about-container {
        width: auto;
        padding: 10rem 20%;
    }

    .text-about-container > p {
        font-size: xx-large;
    }

}

</style>