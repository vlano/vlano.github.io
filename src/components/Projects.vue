<template>
  <section>
    <span>My recent <colored>projects</colored></span>
    <div id="projectContainer">
      <Project title="Augmedit" description="A Mixed Reality software developed for the Microsoft HoloLens 2  with an accompanying website that enables surgeons to
            share holograms with patients and to
            effectively train medical staff and improve surgical planning."
               imageUrl="/projectPhotos/Augmedit/holo.png" siteUrl="https://www.augmedit.com"/>
      <Project title="zMed" description="An innovative medical augmented reality software created in Unity that is based on the of 3D
            visualization
            of
            medical scans that aims to strengthens the doctor-patient relationship and improve the medical
            education." imageUrl="/projectPhotos/zMed/promo.png" siteUrl="https://zmed.hu"/>
      <Project title="Terminal Digit" description="Developed a cross-platform front-end for an application using Angular and Ionic that optimizes the production and
            waste-management of shutter factories, while making the employees work easier with visualizations and easy
            to
            understand instructions." imageUrl="/projectPhotos/TDT/banner.png" siteUrl="https://terminaldigit.tech"/>
      <Project title="Busó Udvar" description="Made an interactive experience for the exhibition where visitors can sit in a boat and row to the other
            side
            of the river. They can control the in-game peddles with real life ones."
               imageUrl="/projectPhotos/BusoUdvar/rowing.png" siteUrl="https://www.facebook.com/busoudvar/"/>
      <Project title="Sokac Ház" description="Made a couple of interactive applications for the exhibiton where visitors can see what they would look
            like
            in
            traditional folk outfit and they could control a virtual folk-band based on traditional musical instrument
            stems." imageUrl="/projectPhotos/SokacHaz/instruments.png"
               siteUrl="http://www.mohacsisokackor.hu/interaktiv-kiallitohely_en/"/>
    </div>
  </section>
</template>

<script>
import Project from "./Project.vue";

export default {
  name: "Projects",
  components: {Project}
}
</script>

<style scoped>
section {
  width: 100%;
}

#projectContainer {
  color: var(--white);
  font-size: 24px;
  padding: 6.25rem;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

span {
  display: block;
  font-weight: 700;
  font-size: 5rem;
  line-height: 7rem;
  letter-spacing: 0.05rem;
  padding: 5rem 0rem 0rem 9rem;
  margin: 0;
}

colored {
  color: var(--turquoise);
}

@media screen and (max-width: 900px) {
  #projectContainer {
    color: var(--white);
    font-size: 2rem;
    padding: 5vw;
    display: flex;
    gap: 2rem;
    flex-wrap: wrap;
    justify-content: center;
  }

  span {
    display: block;
    font-weight: 700;
    font-size: 2rem;
    line-height: 7rem;
    letter-spacing: 0.05rem;
    margin: 0;
    padding: 2rem 0 0;
    width: 100%;
    text-align: center;
  }
}
</style>