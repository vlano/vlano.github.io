<template>
  <section>
    <div>© Norbert Vladika</div>
    <div class="socials">
      <img src="/linkedin-icon.svg" @click="OpenLink(`https://www.linkedin.com/in/norbertvladika/`)">
      <img src="/github-icon.svg" @click="OpenLink(`https://github.com/vlano`)">
      <img src="/mailIcon.svg" @click="OpenMail(`norbert.vladika@gmail.com`)">
    </div>
  </section>
</template>

<script setup>
function OpenLink(url) {
  window.open(url, '_blank');
}

function OpenMail(url) {
  window.location.href = `mailto: ${url}`;
}
</script>

<style scoped>
section {
  font-weight: 400;
  font-size: 1.5rem;
  line-height: 3rem;
  padding-left: 9rem;
  padding-right: 9rem;
  display: flex;
  align-items: center;
  height: 10rem;
  background-color: var(--dark-grey);
}

.socials {
  margin-left: auto;
  display: flex;
  gap: 1rem;
  justify-content: flex-end;
}

img {
  height: 2rem;
  width: 2rem;
  cursor: pointer;
}
</style>