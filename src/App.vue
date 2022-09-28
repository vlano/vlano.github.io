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
  if (document.body.scrollTop > 60 || document.documentElement.scrollTop > 60) {
    document.getElementById("navbar").style.backgroundColor = "rgba(0, 0, 0, 0.6)";
    document.getElementById("navbar").style.paddingTop = "0";
    document.getElementById("logo").style.height = "40px";
  } else {
    document.getElementById("navbar").style.backgroundColor = "transparent";
    document.getElementById("navbar").style.paddingTop = "4.5rem";
    document.getElementById("logo").style.height = "100px";
  }
}
</script>

<template>
  <nav id="navbar">
    <div id="menuContainer">
      <img id="logo" src="/logo.svg" @click="ScrollToTop()"/>
      <a href="#header">Home</a>
      <a href="#skills">Skills</a>
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
    <div id="gradientDiv"><img src="/design/VrGuy.png"></div>
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
  height: 45rem;
  position: relative;
  background-color: var(--dark-blue);
  display: flex;
  flex-direction: column;
  padding-left: 9rem;
  padding-top: 12rem;
  padding-bottom: 12rem;
  gap: 2.5rem;
}

#gradientDiv {
  position: absolute;
  top: 0;
  right: 0;
  width: 50%;
  height: 100%;
  background: radial-gradient(50% 50% at 50% 50%, var(--pink) 0%, var(--dark-blue) 100%);
}

#gradientDiv img {
  height: 100%;
  width: auto;
  position: absolute;
  right: 0;
  bottom: 0;
}

#mainText {
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
  align-items: start;
  display: flex;
  flex-direction: row;
  gap: 3.5rem;
  padding-left: 1rem;
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
  height: 100px;
  width: 100px;
  position: absolute;
  left: 9rem;
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
</style>
