<template>
  <div>
    <h1>页面1</h1>
    <router-link :to="{ name: 'personal', params: { id: 1111}}">标签params传参</router-link><br>
    <router-link :to="{ path: '/personal', query: { id: 1111}}">标签query传参</router-link>
    <div @click="send()">方法params传参</div>
    <div @click="send2()">方法query传参</div>
  </div>
</template>

<script>

export default {
  data() {
    return {

    }
  },
  methods: {
    send() {
      this.$router.push({
        name: 'personal',
        params: {
          id: '1',
          uname: 'myj'
        }
      })
    },
    send2() {
      this.$router.push({
        path: '/personal',
        query: {
          id: '1',
          uname: 'myj'
        }
      })
    }
  },
  components: {

  }
}
</script>

<style>
</style>
