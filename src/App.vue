<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/abr.jpg">
    <HelloWorld msg="Welkom bij Marsmansenbord" @numberClick="numberClicked"/>
    <modal v-if="this.isDisplayStartQuestion" @drink="closeStartQuestionDrink" @laf="closeStartQuestionLaffeBorrelaar">
    </modal>
    <numberModel v-if="this.isDisplayNumberModel" v-bind:clickedNumber="clickedNumber" v-bind:isDrinkGame="isDrinkGame"
                 @close="isDisplayNumberModel = false">
    </numberModel>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import modal from './components/Modal.vue'
import numberModel from './components/NumberModal.vue'

export default {
  name: 'App',
  data() {
    return {
      isDrinkGame: false,
      isDisplayStartQuestion: true,
      isDisplayNumberModel: false,
      clickedNumber: null
    };
  },
  components: {
    HelloWorld,
    modal,
    numberModel
  },
  methods: {
    closeStartQuestionDrink(){
      this.isDrinkGame = true;
      this.isDisplayStartQuestion = false;
    },
    closeStartQuestionLaffeBorrelaar(){
      this.isDrinkGame = false;
      this.isDisplayStartQuestion = false;
    },
    numberClicked(number){
      this.isDisplayNumberModel = true;
      this.clickedNumber = number;
    }
  },
  created: function() {
    this.isDisplayStartQuestion = true;
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
