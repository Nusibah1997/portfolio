<template>
  <svg
    viewBox="0 0 200 200"
    xmlns="http://www.w3.org/2000/svg"
    class="max-w-sm ml-20 self-center"
  >
    <mask id="mask">
      <path fill="#fff" d="M30.3,-56C37.7,-48.2,41,-36.9,44,-27C47,-17,49.8,-8.5,50.3,0.3C50.8,9.1,49,18.2,46.2,28.5C43.4,38.8,39.6,50.4,31.7,60.7C23.8,71,11.9,80.1,2.4,76C-7.2,71.9,-14.3,54.5,-26,46.4C-37.7,38.3,-53.9,39.4,-64.5,33.2C-75.2,27,-80.2,13.5,-82.1,-1.1C-84,-15.6,-82.6,-31.3,-74.6,-42.1C-66.7,-53,-52.2,-59.1,-38.6,-63.3C-25.1,-67.6,-12.5,-70,-0.5,-69.1C11.5,-68.2,22.9,-63.9,30.3,-56Z" transform="translate(100 100)" />
    </mask>
    <image href="/image/color.jpg" width="170" height="200" mask="url(#mask)" class="im" />
  </svg>
</template>

<script>
export default {
  name: 'PhotoP',
  data () {
    return {
    }
  }
}
</script>

<style scoped>
.self-center {
  align-self: center;
  opacity: 0.25;
}
.max-w-sm {
  max-width: 15rem;
}
.ml-20 {
  margin-left: 22rem;
}
</style>
