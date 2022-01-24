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

<style>
.container{
  max-width: 1200px;
  margin: 0 auto;
}
.vueForm{
  border: 1px solid black;
  background-color: rgb(193, 235, 195);
  background-size: cover;
  background-repeat: no-repeat;
  margin-top: 50px;
  padding-top: 50px;
}

</style>