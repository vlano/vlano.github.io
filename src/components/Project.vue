<template>
  <article @click='OpenLink'>
    <header>{{ title }}</header>
    <span>{{ description }}</span>
    <span class="link">Visit ➔</span>
    <img :src="imageUrl"/>
  </article>
</template>

<script setup>
const props = defineProps({
  title: String,
  description: String,
  imageUrl: String,
  siteUrl: String
})

function OpenLink() {
  window.open(props.siteUrl, '_blank');
}
</script>

<style scoped>
img {
  position: absolute;
  background-color: var(--turquoise);
  bottom: 0;
  right: 0;
  width: 30rem;
  height: 30rem;
  filter: grayscale(100%);
  transition: 0.5s;
}

article {
  transition: 0.5s;
  height: 53rem;
  width: 48rem;
  min-width: 48rem;
  position: relative;
  border: 0.2rem solid var(--turquoise);
  border-radius: 0.4rem;
  margin: 3rem;
  cursor: pointer;
}

article:hover {
  background-color: rgba(40, 41, 96, 0.34);;
}

article:hover img {
  filter: grayscale(0%);
}

header {
  text-transform: uppercase;
  font-size: 3rem;
  padding: 3rem;
}

span {
  max-width: 62%;
  display: block;
  font-size: 1.5rem;
  line-height: 2rem;
  padding-left: 3rem;
}

.link {
  letter-spacing: 0.2rem;
  text-transform: uppercase;
  position: absolute;
  bottom: 26rem;
}

.link:hover {
  cursor: pointer;
}

@media screen and (max-width: 900px) {
  img {
    position: absolute;
    background-color: var(--turquoise);
    bottom: 0;
    right: 0;
    width: 15rem;
    height: 15rem;
    filter: grayscale(100%);
    transition: 0.5s;
  }

  article {
    transition: 0.5s;
    height: 44rem;
    width: 100%;
    min-width: 0rem;
    position: relative;
    border: 0.4rem solid var(--turquoise);
    border-radius: 0.8rem;
    margin: 0;
    cursor: pointer;
  }

  article:hover {
    background-color: rgba(40, 41, 96, 0.34);;
  }

  article:hover img {
    filter: grayscale(0%);
  }

  header {
    text-transform: uppercase;
    font-size: 2rem;
    width: 16rem;
    padding-left: 3rem;
    padding-top: 3rem;
    padding-right: 0;
  }

  span {
    max-width: 65vw;
    display: block;
    font-size: 1rem;
    line-height: 1.5rem;
    padding-left: 3rem;
  }

  .link {
    letter-spacing: 0.2rem;
    text-transform: uppercase;
    position: absolute;
    bottom: 16rem;
  }

  .link:hover {
    cursor: pointer;
  }
}
</style>