<template>
  <div>
    <h2>页面2</h2>
    <headerTop></headerTop>
    <div>姓名：{{name}}</div>
    <div>id：{{id}}</div>
    <hr>
    <div>姓名2：{{name2}}</div>
    <div>id2：{{id2}}</div>
  </div>
</template>

<script>
import headerTop from '@/components/headerTop'
export default {
  data() {
    return {
      name: '',
      id: 0,
      name2: '',
      id2: 0
    }
  },
  components: {
    headerTop
  },
  methods: {
    receive() {
      this.name = this.$route.params.uname
      this.id = this.$route.params.id
    },
    receive2() {
      this.name2 = this.$route.query.uname
      this.id2 = this.$route.query.id
    }
  },
  mounted() {
    this.receive()
    this.receive2()
  }
}
</script>

<style>
</style>
