<template>
  <div class="hardware">
    <h1>Hardware 🖥️</h1>
    <p>My current computer hardware is:</p>
    <ul class="ol">
      <li class="li">CPU: Intel(R) Core(TM) i7 CPU 950 @ 3.07GHz</li>
      <li class="li">GPU: GF114 [GeForce GTX 560 Ti]</li>
      <li class="li">RAM: 16gb</li>
      <li class="li">Motherboard: Rampage III Extreme</li>
    </ul>
    <ul>
      <li>
        <router-link to="/">Home</router-link>
      </li>
      <li>|</li>
      <li>
        <router-link to="/about">About</router-link>
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
.hardware {
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
  .ol {
    flex-direction: column;
    .li {
      list-style: square;
      padding: 0px;
      font-size: 15px;
    }
    padding-bottom: 80px;
    padding-left: 50px;
  }
}

ul {
  display: flex;
  justify-content: center;
  padding-bottom: 20px;
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
  .hardware {
    width: 70%;
  }
}
</style>
