<template>
    <div class="about">
        <Menu></Menu>
        <TextAboutContainer text="texto" ></TextAboutContainer>
        <img src="../assets/LRF(73).png" alt="image">
        <TextAboutContainer text="texto" ></TextAboutContainer>
        <TextAboutContainer text="texto" ></TextAboutContainer>
        <img src="../assets/LRF(7).png" alt="image">
    </div>
</template>
<script>

import TextAboutContainer from '@/components/text-about-container.vue';
import Menu from '@/components/menu.vue'

export default {
  name: 'AboutView',
  components: {
    TextAboutContainer,
    Menu
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

.about {
    width: 100vw;
    height: auto;
    background-color: var(--epic-black);
}

.about > img {
  margin: 0 20%;
  margin-top: 3rem;
  width: 60%;
  height: 40%;
  overflow: hidden;
  border-radius: 8px;
}

</style>
