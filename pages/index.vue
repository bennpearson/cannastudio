<template>
  <div class="container">
    <div>
      <Header :title="title" />
      <main>
        <Intro :subtitle="subtitle" />
        <ul class="cs-services">
          <li v-for="(service, index) in services" :key="index">
            <Service :items="service" />
          </li>
        </ul>
      </main>
      <Footer :footer="footer" />
    </div>
  </div>
</template>

<script>
import Header from '~/components/Header.vue'
import Intro from '~/components/Intro.vue'
import Service from '~/components/Service.vue'
import Footer from '~/components/Footer.vue'

export default {
  components: {
    Header,
    Intro,
    Service,
    Footer
  },
  data() {
    return {
      title: 'Canna Studio',
      subtitle: 'We design and build web products',
      services: [
        {
          title: 'Design Systems',
          desc: `Quality, cohesive, maintainable, iterative.
            Design Systems are essential for teams to maintain consistency,
            efficiency and improve quality across multiple projects and products.
            We've been implementing these into both the public and
            private sector since 2009 so have the expertise to get them right.`,
          examples: [
            {
              title: 'Government Digital Transformation',
              desc: `We helped the Office for National Statistics
                bring all paper forms online for the 2021 Census,
                producing inclusive service design components which
                could be used by every product within survey data collection and
                were accessible by everyone in the UK.`,
              logo: 'logo-crown'
            },
            {
              title: 'FinTech',
              desc: `We help the financial technology sector optimise its digital services,
                creating conversational user interfaces, user form journeys and design systems.
                Previous clients include GoCo Group, uSwitch and MoneySuperMarket.`,
              logo: 'logo-fintech'
            }
          ]
        },
        {
          title: 'Product Design',
          desc: `We use a data-informed approach to product development to help us learn, iterate,
            and succeed faster. We like to follow an experiment driven product development process
            but can fit into teams that prefer sprint, lean, agile or Kanban.`,
          examples: [
            {
              title: 'BBC',
              desc: `We designed a variety of products for the BBC's groundbreaking Research and Education Space (RES) project to overhaul Britain's educational resources by digitally throwing open the doors of the UK's biggest linked open data collections.`,
              logo: 'logo-bbc'
            },
            {
              title: 'Wales and West Utilities',
              desc: `We designed a web application to help engineers complete utility 
                works safely and efficiently.`,
              logo: 'logo-wwu'
            }
          ]
        },
        {
          title: 'Prototypes',
          desc: `By testing prototypes on users early on you can gain insightful information to help iterate on designs before going into development. They are a must for every product.`
        },
        {
          title: 'Inclusive Design',
          desc: `We believe accessibility is crucial and can improve revenue. We have worked for the RNIB and written on the subject in .net magazine. We can test your products at the world’s leading accessibility centre for world-class usability testing.`
        },
        {
          title: 'Interaction design',
          desc: `With over 15 years experience in Interaction Design and specialist skills in Frontend, HTML, CSS, JS, SASS and VUE, we can turn your ideas into captivating products with exquisite design.`
        },
        {
          title: 'Professional Design Reviews',
          desc: `We can review your products to reveal any shortcomings and advise on how they can be overcome and improved to help you get back on track.`
        }
      ],
      footer: {
        title: 'About',
        desc: `Founded by Benn and Angharad in 2018 after careers 
        spanning 30 years in the public and private sector, 
        Canna Studio is a product design and development studio based in Pontcanna, Cardiff. 
        We believe quality digital services are the key to success and our aim is 
        to help clients optimise their brand, efficiency and therefore revenue, 
        by creating innovative products with exquisite design and accessibility at their core.`
      }
    }
  }
}
</script>

<style>
html {
  background: black;
  /* background: linear-gradient(
      180deg,
      rgba(2, 0, 47, 0.8),
      rgba(255, 0, 0, 0.05) 70.71%
    ),
    linear-gradient(127deg, rgba(82, 0, 62, 0.8), rgba(0, 1, 25, 0.81) 70.71%),
    linear-gradient(336deg, rgb(0, 0, 45), rgba(0, 0, 255, 0) 70.71%); */
  color: white;
}
body,
input {
  font-family: 'public_sans', 'Helvetica Neue', Arial, sans-serif;
}
.container {
  margin: 0 auto;
  min-height: 100vh;
}
.cs-services {
  list-style-type: none;
  padding: 0;
}
@font-face {
  font-family: 'public_sans';
  src: url('../assets/fonts/publicsans-bold-webfont.woff2') format('woff2');
  font-weight: bold;
}
@font-face {
  font-family: 'public_sans';
  src: url('../assets/fonts/publicsans-regular-webfont.woff2') format('woff2');
  font-weight: normal;
}
@font-face {
  font-family: 'public_sans';
  src: url('../assets/fonts/publicsans-thin-webfont.woff2') format('woff2');
  font-weight: 100;
}
</style>
