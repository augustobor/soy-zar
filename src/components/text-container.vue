<template>
    <div class="text-container" :style="{ color: this.color }">
        <p :style="{ color: this.color }">{{ this.text }}</p>
    </div>
</template>

<script>
export default{
    name: 'text-container',
    props: {
        text: String,
        color: String
    }
}
</script>

<style>
@import '../styles/config.css';

.text-container {
    border-style: solid;
    border-width: 0.2rem;
    box-shadow: 4px 4px 20px;
    padding: 2%;
    width: auto;
    margin: 1rem 10%;
    margin-top: 4rem;
    text-align: center;
}

.text-container > p{
    font-size: large;
}

@media screen and (min-width: 760px) {
    
    .text-container{
        border-width: 0.5rem;
        width: 40%;
        margin: 1rem 30%;
        margin-top: 6rem;
    }

    .text-container > p {
        font-size: xx-large;
    }

}

@media screen and (min-width: 1024px) {

    .text-container {
        width: auto;
        margin: 10rem 20%;
        padding: 1%;
    }

    .text-container > p{
        font-size: xx-large;
    }

}

</style>