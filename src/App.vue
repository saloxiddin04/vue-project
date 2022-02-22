<template>
  <v-app>
    <!--header-->
    <Header/>

    <v-main>
      <!--hero section-->

      <Hero/>
      <!--about section-->
      <About/>

      <!--portfolio section-->
      <Portfolio/>

      <!--project section-->
      <Project/>

      <!--gallery section-->
      <Gallery/>

      <!--contact section-->
      <Contact/>

      <!--footer section-->
      <Footer/>
    </v-main>
  </v-app>
</template>

<script>

import Header from '@/components/Header';
import Hero from "@/components/Hero";
import About from "@/components/About"
import Portfolio from "@/components/Portfolio";
import Project from "@/components/Project";
import Gallery from "@/components/Gallery";
import Contact from "@/components/Contact";
import Footer from "@/components/Footer";

export default {
  name: 'App',
  components: {
    Header,
    Hero,
    About,
    Portfolio,
    Project,
    Gallery,
    Contact,
    Footer
  },

  data() {
    return{
      menus: [
        {title: 'Home', route: 'home'},
        {title: 'About Us', route: 'about-us'},
        {title: 'Portfolio', route: 'portfolio'},
        {title: 'Project', route: 'project'},
        {title: 'Gallery', route: 'gallery'},
        {title: 'Contact', route: 'contact'},
      ]
    }
  }
};
</script>
