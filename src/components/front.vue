<script setup lang="ts">
import { ref } from "vue";

let accountClick = ref(false);
let searchbarActive = ref(false);
let text = ref("");

function searchDel() {
  text.value = "";
}

function searchEnter() {
  if (text.value.length > 0) {
    window.location.replace(`https://google.com/search?q=${text.value}`);
  }
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
          <div
            class="front-bar"
            :class="{
              searchActive: searchbarActive,
              'front-bar-active': searchbarActive,
            }"
          >
            <div class="front-bar-cont">
              <i class="fa-solid fa-magnifying-glass"></i>
              <input
                type="text"
                @keyup.enter="searchEnter"
                v-model="text"
                @blur="searchbarActive = !searchbarActive"
                @focus="searchbarActive = !searchbarActive"
              />
              <div
                class="searchresult"
                :class="{ searchresultGay: searchbarActive }"
              >
                <div class="results">
                  <div class="searchresult-result">
                    <i class="fa-regular fa-clock"></i>
                    <span>hur äcklig är plex?</span>
                  </div>
                  <div class="searchresult-result">
                    <i class="fa-regular fa-clock"></i>
                    <span>Vilken stad har flest orrar?</span>
                  </div>
                  <div class="searchresult-result">
                    <i class="fa-regular fa-clock"></i>
                    <span>Hur äckliga är grekar?</span>
                  </div>
                  <div class="searchresult-result">
                    <i class="fa-regular fa-clock"></i>
                    <span>vaxkev gay?</span>
                  </div>
                  <div class="searchresult-result">
                    <i class="fa-regular fa-clock"></i>
                    <span>fbrp leak?</span>
                  </div>
                  <div class="searchresult-result">
                    <i class="fa-regular fa-clock"></i>
                    <span>hur doxxar jag elevateroleplay?</span>
                  </div>
                  <div class="searchresult-result">
                    <i class="fa-regular fa-clock"></i>
                    <span>Är plex gravid</span>
                  </div>
                  <div class="searchresult-result">
                    <i class="fa-regular fa-clock"></i>
                    <span>elevate roleplay fbrp script?</span>
                  </div>
                  <div class="searchresult-result">
                    <i class="fa-regular fa-clock"></i>
                    <span>Fivem fusk och doxare</span>
                  </div>
                  <div class="searchresult-result">
                    <i class="fa-regular fa-clock"></i>
                    <span>Är 1cm slak normalt?</span>
                  </div>
                </div>
                <div class="searchresult-button">
                  <div class="search-buttons">
                    <button>Sök på google</button>
                    <button>Jag har tur</button>
                  </div>
                </div>
              </div>
            </div>
            <div class="front-bar-cont">
              <div
                class="search-none searchnoneActive"
                v-if="text.length !== 0"
                @click="searchDel"
              >
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
