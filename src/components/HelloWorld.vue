<template>
  <div>
    <svg>
      <circle @click="clickSvg" ref="circle" id="mycircle" cx="50" cy="50" r="50" class="red-circle" />
    </svg>
    <svg class="svg-circle" viewBox="0 0 100 100">
      <circle cx="50" cy="50" r="50" class="fancy"/>
    </svg>
    <svg width="300" height="180">
      <line x1="0" y1="0" x2="200" y2="0" style="stroke:rgb(0,0,0);stroke-width:5" />
    </svg>
    <svg width="300" height="180">
      <polyline points="3,3 30,28 3,53" fill="none" stroke="black" />
    </svg>
    <svg width="300" height="180">
      <rect x="0" y="0" height="100" width="200" style="stroke: #70d5dd; fill: #dd524b" />
    </svg>
    <svg width="300" height="180">
      <ellipse cx="60" cy="60" ry="40" rx="20" stroke="black" stroke-width="5" fill="silver"/>
    </svg>
    <svg width="300" height="180">
      <polygon fill="green" stroke="orange" stroke-width="1" points="0,0 100,0 100,100 0,100 0,0"/>
    </svg>
    <svg width="300" height="180">
      <path d="
        M 18,3
        L 46,3
        L 46,40
        L 61,40
        L 32,68
        L 3,40
        L 18,40
        Z
      "></path>
    </svg>
    <svg>
      <path d="
        M 0,0
        L 100,100
        H 200
        V 200
      " style="stroke: black;stroke-width: 3px;fill:none"></path>
    </svg>
    <svg width="350" height="160">
      <g class="layer" transform="translate(60,10)">
        <circle r="5" cx="0"   cy="105" />
        <circle r="5" cx="90"  cy="90"  />
        <circle r="5" cx="180" cy="60"  />
        <circle r="5" cx="270" cy="0"   />

        <g class="y axis">
          <line x1="0" y1="0" x2="0" y2="120" />
          <text x="-40" y="105" dy="5">$10</text>
          <text x="-40" y="0"   dy="5">$80</text>
        </g>
        <g class="x axis" transform="translate(0, 120)">
          <line x1="0" y1="0" x2="270" y2="0" />
          <text x="-30"   y="20">January 2014</text>
          <text x="240" y="20">April</text>
        </g>
      </g>
    </svg>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  methods: {
    clickSvg() {
      this.$refs.circle.classList.add('circle-click')
      this.$refs.circle.setAttribute('cx', '100')
      this.$refs.circle.setAttribute('cy', '100')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  @keyframes mymove
  {
    from {fill: red;}
    to {fill: blue;}
  }
  .svg-circle{
    width: 200px;
    height: 200px;
  }
  .red-circle{
    fill: red;
    transition: all 1s linear;
    animation: mymove 5s infinite alternate;
  }
  .circle-click{
    fill: blue;
  }
  .fancy {
    fill: none;
    stroke: black;
    stroke-width: 3pt;
  }
</style>
