<template>
  <div class="projects">
    <h1>My projects 📜️</h1>

    <ul>
      <li v-for="(project, index) in projects" :key="index">
        <h1>{{project.title}}</h1>
        <h5>{{trimDate(project.date)}}</h5>
        <p>{{project.description}}</p>
        <div class="buttons">
          <button>
            <a :href="project.repo">Repo</a>
          </button>
          <button>
            <a :href="project.demo">Demo</a>
          </button>
        </div>
      </li>
    </ul>
    <navbar />
  </div>
</template>

<script>
import axios from "axios";
import navbar from "@/components/navbar.vue";
import NProgress from "nprogress";

export default {
  components: {
    navbar
  },
  data() {
    return {
      projects: []
    };
  },
  methods: {
    fetchItems() {
      axios
        .get("https://mynewportfolio.herokuapp.com/projects")
        .then(NProgress.start())
        .then(
          response => {
            this.projects = response.data;
            NProgress.done();
          },
          error => {
            console.log(error);
          }
        );
    },
    trimDate(date) {
      date = date.slice(0, 10);
      return date;
    }
  },
  mounted() {
    this.fetchItems();
  }
};
</script>

<style lang="scss" scoped>
.projects {
  padding-top: 50px;
  display: flex;
  flex-direction: column;
  min-height: 80vh;
  width: 70%;
  margin: 0 auto;
}

h1 {
  padding-left: 10px;
}

ul {
  display: flex;
  flex-wrap: wrap;
  padding-bottom: 80px;
}

li {
  display: flex;
  flex-direction: column;
  margin: 0 10px;
  h1 {
    padding-top: 20px;
    padding-bottom: 1px;
    padding-left: 10px;
  }
  h5 {
    padding-left: 10px;
    color: rgb(177, 175, 175);
    padding-bottom: 20px;
    font-size: 12px;
  }
  p {
    display: flex;
    padding-bottom: 10px;
    flex-wrap: wrap;
    padding-left: 10px;
    padding-right: 10px;
    text-align: justify;
  }

  .buttons {
    display: flex;
    justify-content: center;
  }

  button {
    margin: 10px;
    cursor: pointer;
    transition: all 0.3s ease;
    &:hover {
      background: #b7babd;
    }
    padding: 10px;
    border: none;
    border-radius: 5px;
    outline: none;
    background: #d2d6db;
    color: #363d5b;
    font-weight: 700;
  }
  border-radius: 2px;
  border: 0.5px solid rgba(#868686, 0.6);
  margin-top: 50px;
  background: white;
  list-style: none;
  width: 20vw;
}
</style>