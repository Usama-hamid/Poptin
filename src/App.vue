<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>
export default {};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  height: 100vh;
  color: #2c3e50;
}
#app,
.main,
.inner,
.content {
  display: flex;
  justify-content: center;
  align-items: center;
}
.main,
.nested-inner {
  background: #eb8e5f;
}
.main,
.inner,
.nested-inner {
  border-radius: 50%;
}
.inner,
.nested-inner {
  width: 95%;
  height: 95%;
  display: flex;
  justify-content: center;
}
.main {
  width: 40vw;
  height: 40vw;
}

.inner {
  background: white;
}
.nested-inner {
  padding: 1%;
}
.wrapper {
  padding: 1%;
}

.content {
  flex-direction: column;
  padding: 0 8%;
  justify-content: space-between;
  height: 85%;
}
.content .drag {
  height: 100%;
  justify-content: space-between;
  display: flex;
  flex-direction: column;
  text-align: center;
}
.content .drag div p {
  text-align: center;
  color: white;
  font-weight: 600;
  font-size: 2vw;
}
.content .drag div input {
  position: relative;
  background: white;
  border: none;
  color: #2c3e50;
  border-radius: 5px;
  width: 25vw;
  height: 6vw;
  font-size: 2vw;
}
.content .drag div button {
  background: #2c3e50;
  border: none;
  color: white;
  border-radius: 5px;
  width: 50%;
  width: 15vw;
  height: 6vw;
  font-size: 2vw;
  text-transform: uppercase;
}
</style>
