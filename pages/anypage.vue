<template>
  <div>
    <span v-if="show">
      <Tutorial :text="text"/>
    </span>
    <button @click="updateComponent">수정하기</button>
    <nuxt-link :to="{ path: '/'}" replace>마운트</nuxt-link>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      text: 'hello',
      show: true
    }
  },
  methods: {
    updateComponent() {
      this.text='bye'
    },
    unmountComponent() {
      this.show=!this.show
    }
  }
}
</script>
