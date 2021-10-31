<template>
  <q-page class="my-font">
    <div class="header" id="home">
      <q-header reveal class="bg-transparent">
        <q-toolbar class="constrain">

          <q-toolbar-title class="navigation">
            <p @click="this.$router.push('/')" class="navigation-logo">YUVAL<span class="text-primary">SHALOM;</span>
            </p>
          </q-toolbar-title>


          <div class="links">
            <q-btn-group flat v-show="activateMenu">
              <q-btn><a href="#home">Home</a></q-btn>
              <q-btn><a href="#about">About</a></q-btn>
              <q-btn><a href="#projects">Projects</a></q-btn>
              <q-btn><a href="#contact">Contact</a></q-btn>
            </q-btn-group>

            <tasty-burger-button
              :type="buttonType"
              :active="isActive"
              :size="size"
              :color="color"
              :active-color="activeColor"
              v-on:toggle="onToggle"/>
          </div>

        </q-toolbar>
      </q-header>
      <div class="hero">
        <div class="main-header">
          <div class="main-header-text">
            <h1 class="main-header-primary">YUVAL SHALOM</h1>
            <h2 class="main-header-secondary">FULL STACK WEB DEVELOPER</h2>
          </div>
        </div>
      </div>
    </div>

    <q-page-container>
      <div class="about" id="about">
        <div class="about-box">

          <h1 class="primary-text primary-about">About Me</h1>

          <div class="display-flex">
            <p class="secondary-text">
              My name is Yuval Shalom, I’m 23 years old from <span><a href="https://en.wikipedia.org/wiki/Bat_Yam" target="_blank">Bat-Yam, Israel.</a></span>
              <br>
              I play football as a striker in <span><a href="https://www.football.org.il/players/player/?player_id=233242" target="_blank">Maccabi-Yavne F.C.</a></span><br>
              Oh and I’m also a <span><a href="https://www.linkedin.com/in/yuval-shalom-8b64921bb/" target="_blank">full stack web developer</a></span><br>
              After I finished my <span><a href="https://en.wikipedia.org/wiki/Military_Police_Corps_(Israel)" target="_blank">military service,</a></span> I wanted to do something meaningful and enjoyable,
              so I started programming.
              <br>
              I decided to study <span><a href="https://www.youtube.com/watch?v=N775KsWQVkw" target="_blank">computer science</a></span> at HIT.
              <br>
              After one year of studying I took a year brake from the degree so I can
              bring my programming skills to <span><a href="https://www.youtube.com/watch?v=S-AGE8rDs3Q" target="_blank">another level.</a></span>
            </p>
            <div class="profile-picture-container">
              <img class="profile-pic" src="../assets/profilePic.jpg" alt="profile">
              <div class="profile-picture-border"></div>
            </div>
          </div>
          <a href="#" class="btn btn-primary btn-animate">My Resume</a>

          <h1 class="primary-text primary-skills">The technologies I use: </h1>

          <div class="tech-list">
            <div class="tech-list-num1">
              <div class="tech-list-together">
                <p class="tech-list-text">HTML</p>
                <q-linear-progress :value="0.9" class="tech-list-progress"/>
              </div>

              <div class="tech-list-together">
                <p class="tech-list-text">CSS</p>
                <q-linear-progress :value="0.9" class="tech-list-progress"/>
              </div>

              <div class="tech-list-together">
                <p class="tech-list-text">JavaScript</p>
                <q-linear-progress :value="0.7" class="tech-list-progress"/>
              </div>

              <div class="tech-list-together">
                <p class="tech-list-text">Node.js</p>
                <q-linear-progress :value="0.5" class="tech-list-progress"/>
              </div>

              <div class="tech-list-together">
                <p class="tech-list-text">Express.js</p>
                <q-linear-progress :value="0.5" class="tech-list-progress"/>
              </div>

            </div>

            <div class="tech-list-num2">
              <div class="tech-list-together">
                <p class="tech-list-text">Vue.js</p>
                <q-linear-progress :value="0.9" class="tech-list-progress"/>
              </div>

              <div class="tech-list-together">
                <p class="tech-list-text">Vuex</p>
                <q-linear-progress :value="0.8" class="tech-list-progress"/>
              </div>

              <div class="tech-list-together">
                <p class="tech-list-text">Quasar</p>
                <q-linear-progress :value="0.9" class="tech-list-progress"/>
              </div>

              <div class="tech-list-together">
                <p class="tech-list-text">Firebase</p>
                <q-linear-progress :value="0.7" class="tech-list-progress"/>
              </div>

              <div class="tech-list-together">
                <p class="tech-list-text">Git</p>
                <q-linear-progress :value="0.6" class="tech-list-progress"/>
              </div>
            </div>

          </div>
        </div>
      </div>


      <div class="projects" id="projects">
        <div class="about-box about-box-projects contact-box">
          <h1 class="primary-text primary-about">My Projects</h1>

          <div class="project">
            <div class="project-text">
              <p class="project-text-primary">FriendsBook</p>
              <p class="project-text-secondary">A social network built with Vuejs, Vuex, Css, Quasar framework FireBase, Nodejs and Express.</p>
            </div>
            <a href="https://github.com/yuvalysh0/Friendsbook" target="_blank" class="btn-mini btn-primary-mini btn-animate">Github</a>
            <a href="#" class="btn-mini btn-primary-mini btn-animate">Demo</a>
          </div>

          <div class="project">
            <div class="project-text">
              <p class="project-text-primary">Flash Media Scheduler</p>
              <p class="project-text-secondary">This app was built by the flashdev students and I (4 people). We used Vuejs, Vuex, Quasar framework, Firebase, Css, Bitbucket and Jira.</p>
            </div>
            <a href="#" target="_blank" class="btn-mini btn-primary-mini btn-animate">Github</a>
            <a href="#" class="btn-mini btn-primary-mini btn-animate">Demo</a>
          </div>

          <div class="project">
            <div class="project-text">
              <p class="project-text-primary">My Portfolio</p>
              <p class="project-text-secondary">A personal portfolio that was built with Vuejs, Css and Quasar framework</p>
            </div>
            <a href="https://github.com/yuvalysh0/yuval-portfolio" target="_blank" class="btn-mini btn-primary-mini btn-animate">Github</a>
            <a href="#projects" class="btn-mini btn-primary-mini btn-animate" @click="openDialog = true">Demo</a>
            <q-dialog v-model="openDialog">
              <q-card dark class="q-pa-md">
                <q-card-section>
                  <div class="text-h6">Wait a minute</div>
                </q-card-section>

                <q-card-section class="q-pt-none">
                  Well, I guess that this is the actual demo so...
                </q-card-section>

                <q-card-actions align="right">
                  <q-btn flat label="OK" color="primary" v-close-popup />
                </q-card-actions>
              </q-card>
            </q-dialog>
          </div>

        </div>
      </div>

      <div class="contact" id="contact">
        <div class="about-box contact-box">
          <h1 class="primary-text primary-about">Contact Me</h1>
          <div class="contact-form secondary-text">
            <form
              class="q-gutter-md"
              ref="form"
              action="https://formsubmit.co/yuvalysh0@gmail.com"
              method="POST"
            >
              <q-input
                v-model="formData.name"
                name="user_name"
                dark
                filled
                label="Full name*"
                required
              >
                <template v-slot:prepend>
                  <q-icon name="eva-person"/>
                </template>
              </q-input>
              <q-input
                v-model="formData.email"
                name="user_email"
                dark
                filled
                label="Email*"
                required
              >
                <template v-slot:prepend>
                  <q-icon name="eva-email"/>
                </template>
              </q-input>
              <q-input
                dark
                name="message"
                label="Write here whatever you want to ask me :) "
                v-model="formData.text"
                filled
                type="textarea"
                required
              >
                <template v-slot:prepend>
                  <q-icon name="eva-text"/>
                </template>
              </q-input>
              <div>
                <q-btn flat label="Submit" type="submit" color="primary"/>
              </div>
            </form>
          </div>
        </div>
      </div>
      <div class="useful-links">
        <ul>
          <li><a href="https://www.facebook.com/yuval.shalom.980/" target="_blank">
            <q-icon name="eva-facebook" size="md"/>
          </a></li>
          <li><a href="https://www.linkedin.com/in/yuval-shalom-8b64921bb/" target="_blank">
            <q-icon name="eva-linkedin" size="md"/>
          </a></li>
          <li><a href="https://github.com/yuvalysh0" target="_blank">
            <q-icon name="eva-github" size="md"/>
          </a></li>
        </ul>
        <div class="line"></div>
      </div>
    </q-page-container>
    <q-footer reveal>
      <p>Crafted By Me</p>
    </q-footer>

  </q-page>
</template>

<script>
import {TastyBurgerButton} from 'vue-tasty-burgers'
import BackToTop from 'vue-backtotop'

export default {
  data() {
    return {
      formData: {
        name: '',
        email: '',
        text: '',
      },
      openDialog: false,
      activateMenu: false,
      buttonType: 'spin',
      isActive: false,
      size: 's',
      color: 'white',
      activeColor: 'white'
    }
  },
  components: {
    'tasty-burger-button': TastyBurgerButton,
    BackToTop
  },
  methods: {
    onToggle(active) {
      this.activateMenu = !this.activateMenu
    },
    goUp() {
      document.body.scrollTop = 0; // For Safari
      document.documentElement.scrollTop = 0;
    },
  },
}
</script>
