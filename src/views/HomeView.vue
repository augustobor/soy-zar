<template>
  <div class="home">
    <header>
      <img src="../assets/LRF(38).png" alt="header_image">
    </header>
    <Menu></Menu>
    <TextContainer text="texto" color="var(--fresh-red)"></TextContainer>
    <img src="../assets/LRF(79).png" alt="header_image">
    <TextContainer text="texto" color="var(--berry-red)"></TextContainer>
    <PlayerContainer></PlayerContainer>
    <button>escuchar</button> 
    <TextContainer text="texto" color="var(--berry-red)"></TextContainer>
    <section>
      <VideoContainer></VideoContainer>
    </section>
    <TextContainer text="texto" color="var(--shiny-orange)"></TextContainer>
    <footer>
      <address>
        <h2>TikTok</h2>
        <img src="../assets/tik_tok_logo.svg" alt="tik_tok_logo">
      </address>
      <address>
        <h2>Insta</h2>
        <img src="../assets/instagram_logo.svg" alt="insta_logo">
      </address>
    </footer>
  </div>
</template>

<script>
import TextContainer from '@/components/text-container.vue';
import PlayerContainer from '@/components/player-container.vue';
import VideoContainer from '@/components/video-container.vue';
import Menu from '@/components/mobile-menu.vue'

export default {
  name: 'HomeView',
  components: {
    TextContainer,
    PlayerContainer,
    VideoContainer,
    Menu
  }
}
</script>

<style>
@import '../styles/config.css';

.home {
  background-color: var(--epic-black);
}

.home header img {
  width: 100%;
}

.home img{
  width: 85%;
}

button {
  width: 70vw;
  padding: 4%;
  background-color: var(--fresh-red);
  border-style: none;
  font-size: large;
  color: var(--just-white);
  border-radius: 4px;
}

button:hover {
  background-color: var(--shiny-orange);
  transition: all 400ms ease;
}
footer, address {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-around;
}

address {
  margin: 2rem 2rem 1rem 2rem;
}

.home footer h2 {
  color: var(--strong-red);
  font-weight: normal;
}

.home footer img {
  width: 30%;
  height: 30%;
}
</style>
