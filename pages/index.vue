<template>
  <div class="container">
    明若清渊
  </div>
</template>

<script>
const HomeKey = 'Home'
export default {
  components: {},
  created: function() {
    console.log(this.$store.state.modules[HomeKey].name)
  },
  methods: {}
}
</script>

<style>
.container {
  min-height: 100vh;
  width: 100vw;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background: powderblue;
  color: #fff;
  font-size: 27px;
}
</style>
