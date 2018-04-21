<template>
  <div id="app">
    <Header/>
    <Sidebar/>
    <div id="timeline-view">
      <router-view/>
    </div>
  </div>
</template>

<script>
import Sidebar from './components/sidebar'
import Header from './components/header'

export default {
  name: 'App',
  components: {
    Header,
    Sidebar
  }
}
</script>

<style>
* {
  font-family: 'Open Sans', sans-serif;
}

html, body {
  margin: 0;
  height: 100%;
}

#app {
  display: flex;
  flex-direction: row;
  height: 100%;
}

#sidebar {
  flex: 1;
  max-width: 15em;
  border-right: 1px #999 solid;
  padding-top: 1em;
  padding-left: 1em;
  margin-top: 2em;
}

#timeline-view {
  padding: 1em;
  flex: 1;
  overflow-y: scroll;
  margin-top: 3em;
}

a {
  text-decoration: none;
}

a:hover {
  text-decoraiton: underline;
}

h1, h2, h3, h4, h5, h6 {
  margin-top: 0;
}

.btn {
  background: #eee;
  border: none;
  padding: 1em;
  border-radius: 0.5em;
  font-weight: bold;
  color: #000;
}

.btn-small {
  padding: 0.5em;
}

.pull-right {
  float: right;
}

.emoji {
  height: 1em;
}
</style>
