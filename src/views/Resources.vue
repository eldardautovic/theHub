<template>
  <div class="wrapper">
    <h1>Coming soon!</h1>
    <router-link to="/">Go back home ></router-link>
  </div>
</template>

<script>
export default {};
</script>

<style lang='scss'>
.wrapper {
  display: flex;
  min-height: 100vh;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  h1 {
    font-weight: bold;
    padding-bottom: 10px;
    font-style: italic;
  }
  a {
    font-size: 18px;
  }
}
</style>