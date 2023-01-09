<!-- Please remove this file from your project -->
<template>
  <div class="" style="width: 100%;">
    Life Cycle 훅 예제 
    <br />
    {{ text }}
  </div>
</template>

<script>
export default {
  name: 'NuxtTutorial',
  props : {
    text: String
  },
  data() {
    return {
    }
  },

  beforeCreate() { // 컴포넌트 인스턴스 생성 바로 직전에 실행되는 훅
    // this.text = 'beforeCreate'
    console.log('beforeCreated')
  },

  // 1. 생성단계 Vue 컴포넌트 인스턴스를 생성하는 단계 new Vue()

  created() { // 컴포넌트 인스턴스 생성 후에 바로 실행되는 훅
    console.log('created')
  },


  beforeMount() { // 컴포넌트 인스턴스 마운트 바로 직전에 실행되는 훅
    console.log('beforeMount')
  },

  // 2. 마운팅 단계 컴포넌트 생성이 완료 된 후 돔 트리에 렌더링이 되는 단계

  mounted() {
    console.log('mounted')
  },

  beforeUpdate() {
    console.log('beforeUpdate')
  },
  
  // 3. 업데이트 단계 Vue 컴포넌트 변경 시 컴포넌트를 다시 만들어서 변경해서 돔트리에 적용

  updated() {
    console.log('updated')
  },


  beforeUnmount() {
    console.log('beforeUnmount')
  },
  // 4. 언마운트

  unmounted() {
    console.log('unmounted')
  },

}
</script>
