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
        <h2>Instagram</h2>
        <img src="../assets/instagram_logo.svg" alt="insta_logo">
      </address>
    </footer>
  </div>
</template>

<script>
import TextContainer from '@/components/text-container.vue';
import PlayerContainer from '@/components/player-container.vue';
import VideoContainer from '@/components/video-container.vue';
import Menu from '@/components/menu.vue'

export default {
  name: 'HomeView',
  components: {
    TextContainer,
    PlayerContainer,
    VideoContainer,
    Menu,
  },
  data: function() {
      return {
          isDesktop: false
      };
    },
}
</script>

<style>
@import '../styles/config.css';

.home {
  background-color: var(--epic-black);
}

.home header {
  height: 25vh;
  overflow: hidden;
}

.home header img {
  width: 100%;
  height: auto;
}

.home > img {
  margin: 0 25%;
  margin-top: 3rem;
  width: 50%;
  height: 40%;
  overflow: hidden;
  border-radius: 8px;
}

button {
  width: 70vw;
  padding: 4%;
  margin: 0 15%;
  background-color: var(--fresh-red);
  border-style: none;
  font-size: large;
  font-weight: bold;
  color: var(--just-white);
  border-radius: 4px;
  text-align: center;
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
  font-weight: bold;
}

.home footer img {
  width: 30%;
  height: 30%;
}

@media screen and (min-width: 760px) {

  .home header {
    height: 35vh;
  }

  .home header img {
    position: relative;
    top: -50px;
  }

  .home > img {
    margin-top: 5rem;
  }

  button {
    margin-top: 3rem;
    width: 40vw;
    margin: 0 30%;
    padding: 2%;
    font-size: xx-large;
    border-radius: 4px;
  }

  footer {
    margin-top: 3rem;
  }

  .home footer img {
    width: 40%;
    height: 40%;
  }

  footer address h2 {
    font-size: large;
    padding: 2%;
  }

}


@media screen and (min-width: 1024px) {

  .home header {
    height: 50vh;
  }

  .home header img {
    position: relative;
    top: -100px;
  }

  .home > img {
    display: none;
  }

  button {
    width: 20vw;
    margin: 0 39%;
    margin-top: 3rem;
  }

  footer {
    margin-top: 5rem;
  }

  .home footer img {
    width: 100%;
    height: 100%;
  }

  footer address h2 {
    font-size: xx-large;
    padding: 10%;
  }

}
</style>
