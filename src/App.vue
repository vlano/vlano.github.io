<script setup>

import Skills from "./components/Skills.vue";
import Projects from "./components/Projects.vue";
import Contact from "./components/Contact.vue";
import Footer from "./components/Footer.vue";

function OpenLink(url) {
  window.open(url, '_blank');
}

function ScrollToTop() {
  window.scrollTo({
    top: 0,
    behavior: 'smooth'
  });
}

window.onscroll = function () {
  scrollFunction()
};

function scrollFunction() {
  if (window.innerWidth < 900) {
    return;
  }
  if (document.body.scrollTop > 60 || document.documentElement.scrollTop > 60) {
    document.getElementById("navbar").style.backgroundColor = "rgba(0, 0, 0, 0.6)";
    document.getElementById("navbar").style.paddingTop = "0";
    document.getElementById("logo").style.height = "40px";
  } else {
    document.getElementById("navbar").style.backgroundColor = "transparent";
    document.getElementById("navbar").style.paddingTop = "6rem";
    document.getElementById("logo").style.height = "9rem";
  }
}
</script>

<template>
  <nav id="navbar">
    <div id="menuContainer">
      <img id="logo" src="/logo.svg" @click="ScrollToTop()"/>
      <a href="#header">Home</a>
      <a href="#projects">Projects</a>
      <a href="#contact">Contact</a>
    </div>
  </nav>
  <header id="header">
    <div id="mainText">
      <span class="intro">Hi I'm <name>Norbert Vladika</name></span>
      <span class="subText"> I am a software developer specialized in XR and interactive applications.</span>
    </div>
    <div class="socials">
      <img class="link" src="/linkedin-icon.svg" @click="OpenLink(`https://www.linkedin.com/in/norbertvladika/`)">
      <img class="link" src="/github-icon.svg" @click="OpenLink(`https://github.com/vlano`)">
    </div>
    <img id="vrGuy" src="/design/VrGuy.png">
  </header>
  <main>
    <Skills id="skills"/>
    <Projects id="projects"/>
    <Contact id="contact"/>
    <Footer/>
  </main>
</template>

<style scoped>
a {
  text-decoration: none;
  color: var(--white);
}

name {
  color: var(--turquoise);
}

.intro {
  text-shadow: 0px 0px 10px rgba(47, 254, 225, 0.34);
}

header {
  width: 100%;
  height: 100%;
  position: relative;
  background: url("/design/headerBg.svg") no-repeat right;
  background-size: cover;
  display: flex;
  flex-direction: column;
  gap: 2.5rem;
  overflow: hidden;
}

#vrGuy {
  height: 100%;
  width: auto;
  position: absolute;
  right: 0;
  bottom: 0;
}

#mainText {
  margin-top: 24rem;
  margin-left: 9rem;
  font-weight: 700;
  display: flex;
  flex-direction: column;
  align-items: start;
  font-size: 5rem;
  gap: 2.5rem;
  width: 38rem;
  z-index: 10;
}

.subText {
  font-size: 3rem;
  font-weight: 400;
}

.socials {
  margin-left: 9rem;
  align-items: start;
  display: flex;
  flex-direction: row;
  gap: 3.5rem;
  padding-left: 1rem;
  padding-bottom: 4rem;
  z-index: 10;
}

.socials img {
  width: 3.75rem;
  height: 3.75rem;
}

span {
  padding: 1rem;
  justify-content: center;
  align-items: center;
}

nav {
  position: fixed;
  width: 100%;
  padding-top: 4.5rem;
  z-index: 15;
  transition: 0.4s;
}

#logo {
  width: 9rem;
  height: 9rem;
  position: absolute;
  left: 8rem;
  cursor: pointer;
  transition: 0.4s;
}

#menuContainer {
  position: relative;
  margin-right: 9rem;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  flex-direction: row;
  gap: 2.5rem;
  padding: 1rem;
}

nav a {
  font-size: 1.5rem;
  letter-spacing: 0.2rem;
  text-transform: uppercase;
}

nav a:hover {
  color: var(--turquoise);
  cursor: pointer;
}

main {
  background-color: var(--dark-blue);
  display: flex;
  flex-direction: column;
}

img {
  width: 300px;
  height: 300px;
}

.link {
  cursor: pointer;
}

@media screen and (max-width: 900px) {
  nav {
    position: absolute;
    width: 100%;
    padding-top: 0rem;
    z-index: 15;
    transition: 0.4s;
  }

  #menuContainer {
    background: none;
  }

  #menuContainer a {
    display: none;
  }

  header {
    width: 100%;
    height: 100%;
    position: relative;
    background: url("/design/headerBg-mobile.svg") no-repeat right;
    background-size: cover;
    display: flex;
    flex-direction: column;
    gap: 2.5rem;
    overflow: hidden;
  }

  #vrGuy {
    display: none;
  }

  #logo {
    width: auto;
    height: 6rem;
    position: absolute;
    top: 3rem;
    left: 2rem;
    cursor: pointer;
    transition: 0.4s;
  }

  #mainText {
    margin-top: 12rem;
    margin-left: 1rem;
    margin-right: 1rem;
    font-weight: 700;
    display: flex;
    flex-direction: column;
    align-items: start;
    font-size: 3rem;
    gap: 1rem;
    width: 100%;
    z-index: 10;
  }

  .subText {
    font-size: 2rem;
    font-weight: 400;
    margin-right: 1rem;
  }

  .socials {
    margin-left: 1rem;
    align-items: start;
    display: flex;
    flex-direction: row;
    gap: 5rem;
    padding-left: 1rem;
    padding-bottom: 4rem;
    z-index: 10;
  }

  .socials img {
    width: 5rem;
    height: 5rem;
  }
}

</style>
