<template>
  <div>
    <div class="points-init ml-5 opacity-75 absolute z-30 top-60 left-32">
      <span /><span /><span /><span /><span /><span /><span /><span /><span /><span /><span /><span /><span /><span /><span /><span /><span /><span /><span /><span />
    </div>
  </div>
</template>

<script>
export default {
  name: 'PointP'
}
</script>

<style scoped>
.points-init {
  width: 100px;
  height: 100px;
  top: 500px;
  left: 110px;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;
}
.points-init span {
  width: 25px;
  height: 25px;
  display: block;
  transition: all .25s ease;
  display: flex;
  align-items: center;
  justify-content: center;
}
.points-init span:after {
  content: "";
  position: relative;
  width: 6px;
  height: 6px;
  background: #bdbde5;
  border-radius: 50%;
  transition: all .25s ease;
}
.points-init span:hover:after{
  background-color: #4455ff;
}
</style>
