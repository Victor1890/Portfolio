<template>
  <div id="app">
    <!-- ======= Header ======= -->
    <header
      id="header"
      class="fixed-top d-flex justify-content-center align-items-center header-transparent"
    >
      <nav id="navbar" class="navbar">
        <ul>
          <Navigation
            v-for="(i, index) in menuList"
            :title="i.title"
            :href="i.href"
            :key="index"
          />
        </ul>
      </nav>
    </header>
    <Banner :banner="bannerInfo" />
    <About :about="aboutInfo"/>
    <Projects />
    <!--<BannerSecondary/>-->
    <Contact />
    <!-- ======= Footer ======= -->
    <footer id="footer">
      <VueFooter />
    </footer>
  </div>
</template>

<script>
import Navigation from "./components/Navigation.vue";
import VueFooter from "./components/VueFooter.vue";
import Banner from "./components/Banner.vue";
import About from "./components/About.vue";
import Projects from "./components/Projects.vue";
import Contact from "./components/Contact.vue";

export default {
  name: "app",
  data: () => {
    return {
      menuList: [
        { title: "Home", href: "#hero" },
        { title: "Contact me", href: "#Contact" },
      ],

      bannerInfo: {
        name: "Natalie Corniell",
        aboutMe: "- Web Developer in Santo Domingo -",
        photo: 'background: url("../assets/img/me.jpg") top right;',
      },
        aboutInfo: {
        name: "Natalie Corniell",
        aboutMe: "- Web Developer in Santo Domingo -",
        photo: 'background: url("../assets/img/me.jpg") center center no-repeat;',
        website: "https://portfolio-paiisyfkc-nataliecorniell.vercel.app",
        phoneNumber: "(829)-518-9958",
        city: "Santo Domingo",
        linkedIn: "/NatalieCorniell",
        degree: "Software technologist",
        email: "nataliecorniell@gmail.com",
        experience: "1+ year of experience in the area",
        awards: "Microsoft Certified: Azure Fundamentals",
        skills:[{name: 'Scrum', val: 90},{name: 'MVC', val: 90},
         {name: 'VueJs', val: 90}, {name: 'Umbraco CMS', val: 90},
         {name: 'CSharp', val: 90}]
      },
 
    };
  },
  components: {
    Navigation,
    VueFooter,
    Banner,
    About,
    Projects,
    Contact,
  },
};
</script>
