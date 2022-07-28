<template>
  <div id="app">
    <button @click="isDanger = !isDanger">Toggle danger</button>
    <div
      :class="[isDanger ? 'danger' : '', !isDanger ? 'safe' : '', 'large-text']"
      style="margin-top: 15px"
    >
      {{ isDanger ? "Danger" : "Safe" }}
    </div>
    <div class="np-credits">wwww.nightprogrammer.com</div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return { isDanger: false };
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  padding: 24px;
  font-size: 20px;
}

button {
  background-color: #004cbe;
  color: #ffffff;
  border: 0px;
  border-radius: 6px;
  padding: 6px 20px;
  margin-right: 1em;
  cursor: pointer;
  transition: all 0.3s;
}

button:hover {
  background-color: #2f79e7;
  transition: all 0.3s;
}

.np-credits {
  font-size: 12px;
  margin-top: 12px;
  color: #4b4b4b;
}

.danger {
  color: red;
}

.safe {
  color: green;
}

.large-text {
  font-size: 30px;
}
</style>