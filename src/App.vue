<template>
  <div id="app">
    <h2>Привет я сайт 1</h2>
    <AlertOne
      text="Тип: success"
      type="success"
      :isShown="true"
    />
    <div class="spacer" style="height: 30px"></div>
    <AlertOne
      text="Тип: error"
      type="error"
      :isShown="true"
    />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import AlertOne from './components/AlertOne.vue'

@Component({
  components: { AlertOne }
})
export default class App extends Vue {}
</script>

<style>
#app {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

</style>
