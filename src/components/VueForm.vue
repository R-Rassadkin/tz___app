<template>
  <div class="vueForm">
    <div class="container">
        <CheckBox></CheckBox>
        <ListWords></ListWords>
    </div>
  </div>
</template>

<script>
import CheckBox from '@/components/CheckBox.vue'
import ListWords from '@/components/ListWords.vue'
export default {
  components: {
  CheckBox,
  ListWords
  }
}
</script>

<style lang="scss">

@import '@/assets/style/vueForm.scss'

</style>