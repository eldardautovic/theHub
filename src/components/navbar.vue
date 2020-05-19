<template>
  <div class="hello">
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
        <router-link to="/">Home</router-link>
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
  name: "Nav"
};
</script>

<style scoped lang="scss">
ul {
  width: 32%;
  margin: 0 auto;
  display: flex;
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
</style>
