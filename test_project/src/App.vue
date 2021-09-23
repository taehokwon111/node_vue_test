<template>
  <div id="app">
    <header>
      <ul>
        <li><span>decideCnt</span></li>
        <li><span>clearCnt</span></li>
        <li><span>deathCnt</span></li>
        <li><span>examCnt</span></li>
      </ul>

    </header>
    <main>
      <router-view></router-view>
    </main>
  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>

<style>
*{margin: 0 auto;}

body {
  margin: 0;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

main {
  text-align: center;
  margin-top: 40px;
}
ul{
  display: flex;
  justify-content: space-between;
}
header {
  margin: 0px;
  height: 70px;
  padding: 0 16px 0 24px;
  background-color: #35495E;
  color: #ffffff;
}

header span {
  display: block;
  position: relative;
  font-size: 20px;
  line-height: 1;
  letter-spacing: .02em;
  font-weight: 400;
  box-sizing: border-box;
  padding-top: 24px;
}
</style>
