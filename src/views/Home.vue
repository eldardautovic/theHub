<template>
  <div class="home">
    <h2>Welcome to the hub! 🤗️</h2>
    <h4>What is the purpose of this "hub"? 🤔️</h4>
    <p>
      The purpose of this hub is to make sure I share my cool resources and projects more easily
      than I used to. The next thing I wanted to make sure is to showcase my projects and my hardware setup more proficiently.
      Getting as much people as I can to find the way to solve their problem is my goal with this website.
      This is one of my first fullstack projects in my constant period of learning to code.
      Have fun with using this site, there is nothing else to say! 👋️
    </p>
    <ul>
      <li>
        <router-link to="/about">About</router-link>
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

<script>
export default {
  name: "Home"
};
</script>


<style lang="scss">
.home {
  width: 50%;
  margin: 0 auto;
  min-height: 80vh;
  display: flex;
  justify-content: center;
  flex-direction: column;
  h2 {
    padding-bottom: 40px;
    font-weight: 600;
  }
  h4 {
    padding-bottom: 20px;
    font-size: 18px;
  }
  p {
    text-align: justify;
    padding-bottom: 80px;
  }
}

ul {
  display: flex;
  padding-bottom: 20px;
  justify-content: center;
}

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

@media only screen and (max-width: 700px) {
  .home {
    width: 70%;
  }
}
</style>