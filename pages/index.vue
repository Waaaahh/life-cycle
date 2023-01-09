<template>
  <div>
    <div>
      <img style="width: 1000px" :src="require(`~/assets/vue-lifecycle.png`)"/>
    </div>
    <span v-if="show">
      <Tutorial :text="text"/>
    </span>
    <button @click="updateComponent">수정하기</button>
    <button @click="unmountComponent">토글마운트</button>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      text: '수정 전',
      show: true
    }
  },
  methods: {
    updateComponent() {
      this.text='수정 후'
      setTimeout(() => this.text='수정 전', 5000)
    },
    unmountComponent() {
      this.show=!this.show
    }
  }
}
</script>
