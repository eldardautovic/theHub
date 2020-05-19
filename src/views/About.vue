<template>
  <div class="about">
    <h1>About 💥️</h1>
    <p>
      Hello! My name is Eldar Dautovic. I am the creator and the developer behind this hub.
      This hub has a goal to help people get my latest projects faster and easier.
      I'm trying to make my projects dynamic so I can add them easily and also the resources.
      Adding lots of resources dynamically can help me do faster and better work!
      Helping people find what they are looking for and generally solving their problems is what I'm looking to do.
      Anyone that I help out with finding what they look for is one more advantage.
      This site is written in Vue.js as a Front End and node.js in combination with express.js and MongoDB for the backend. 🤩️
    </p>Contact:
    <ol class="contact">
      <li>
        <a href="https://github.com/SalesmanUnknown">
          <i class="fab fa-github"></i>
        </a>
      </li>
      <li>
        <a href="https://www.linkedin.com/in/eldardautovic/">
          <i class="fab fa-linkedin"></i>
        </a>
      </li>
      <li>
        <a href="mailto:dautoviceldar20@gmail.com">
          <i class="fas fa-envelope"></i>
        </a>
      </li>
    </ol>
    <ul class="nav">
      <li>
        <router-link to="/">Home</router-link>
      </li>
      <li>|</li>
      <li>
        <router-link to="/hardware">Hardware</router-link>
      </li>
      <li>|</li>
      <li>
        <router-link to="/projects">Projects</router-link>
      </li>
      <li>|</li>
      <li>
        <router-link to="/resources">Resources</router-link>
      </li>
    </ul>
  </div>
</template>

<style lang="scss" scoped>
.about {
  display: flex;
  flex-direction: column;
  justify-content: center;
  min-height: 80vh;
  width: 50%;
  margin: 0 auto;

  h1 {
    padding-bottom: 40px;
  }
  p {
    text-align: justify;
    padding-bottom: 20px;
  }
  .contact {
    padding-bottom: 80px;
    padding-left: 50px;
    padding-top: 10px;
    display: flex;
    li {
      list-style: none;
      font-size: 20px;
      &:nth-child(even) {
        padding: 0px 10px;
      }
    }
  }
}

.nav {
  display: flex;
  justify-content: center;
  padding-bottom: 20px;
  li {
    font-size: 0.8em;
    list-style: none;
    &:nth-child(even) {
      padding: 0px 10px;
    }
    &:first-child {
      padding: 0px;
    }
    &:last-child {
      padding: 0px;
    }
  }
}

@media only screen and (max-width: 700px) {
  .about {
    width: 70%;
  }
}
</style>
