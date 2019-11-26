<template>
  <q-page class="flex flex-center">
    <div>我的版本号为:0.0.3</div>
    <div id="messages"></div>
  </q-page>
</template>

<script>
// Display the current version
// let version = window.location.hash.substring(1);
// document.getElementById("version").innerText = version;
// Listen for messages
const { ipcRenderer } = require("electron");
ipcRenderer.on("message", function(event, text) {
  debugger;
  var container = document.getElementById("messages");
  var message = document.createElement("div");
  message.innerHTML = text;
  container.appendChild(message);
});
export default {
  name: "PageIndex"
};
</script>
