<template>
  <div class="content">
    <div class="icons -outline">
      <div
        v-for="(item, index) in outlineIcons"
        v-html="item.svg"
        :key=item.name
      />
    </div>
    <div class="icons -filled">
      <div
        v-for="(item, index) in filledIcons"
        v-html="item.svg"
        :key=item.name
      />
    </div>
  </div>
</template>

<script>
import * as outlineIcons from "@bitcoin-design/bitcoin-icons-svg/outline/index.js";
import * as filledIcons from "@bitcoin-design/bitcoin-icons-svg/filled/index.js";

export default {
  name: 'App',
  components: {
  },

  data() {
    return {
      outlineIcons,
      filledIcons
    }
  }
}
</script>

<style>
#app {
  font-family: sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  padding: 40px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.content {
  display: flex;
  flex-direction: column;
  flex-basis: 800px;
  flex-grow: 0;
  max-width: 800px;
  gap: 40px;
}

.icons {
  display: flex;
  flex-wrap: wrap;
}

.icons div {
  padding: 5px;
}

.icons div svg {
  width: 30px;
  height: 30px;
}
</style>
