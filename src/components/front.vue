<script setup lang="ts">
import { ref } from "vue";

let accountClick = ref(false);

function clickey() {
  console.log("Hej");
}
</script>

<template>
  <div class="front-wrapper">
    <div class="front-container">
      <div class="front-navbar">
        <span>Gmail</span>
        <span>Bilder</span>
        <div
          class="dots"
          v-on:click="accountClick = !accountClick"
          :class="{ accountActive: accountClick }"
        >
          <i class="fa-solid fa-ellipsis-vertical"></i
          ><i class="fa-solid fa-ellipsis-vertical"></i
          ><i class="fa-solid fa-ellipsis-vertical"></i>
        </div>
        <img />
      </div>
      <div class="front-search-container">
        <div class="front-search">
          <img
            src="https://www.google.com/logos/doodles/2022/seasonal-holidays-2022-6753651837109831.8-ladc.gif"
            alt=""
          />
          <div class="front-bar">
            <i class="fa-solid fa-magnifying-glass"></i>
            <input type="text" />
            <div class="search-none">
              <i class="fa-solid fa-xmark"></i>
              <span class="front-search-none-span"></span>
            </div>
            <div class="front-search-bild">
              <img
                src="https://www.gstatic.com/inputtools/images/tia.png"
                alt=""
              />
              <i class="fa-solid fa-microphone-lines"></i>
              <i class="fa-solid fa-camera-retro"></i>
            </div>
          </div>
          <div class="search-buttons">
            <button>Sök på google</button>
            <button>Jag har tur</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
