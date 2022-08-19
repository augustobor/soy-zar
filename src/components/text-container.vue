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

.text-container{
    border-style: solid;
    border-width: 0.2rem;
    box-shadow: 4px 4px 20px;
    padding: 2%;
    width: auto;
    margin: 1rem 10%;
}

.text-container > p{
    font-size: large;
}
</style>