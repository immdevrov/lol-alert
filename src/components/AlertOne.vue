<script lang="ts">
import { Component } from 'vue-property-decorator'
import Alert from './AlertParent.vue'

@Component
export default class AlertOne extends Alert {}

</script>
<style scoped>

.alert-wrapper {
  --success-color: rgb(1, 88, 1);
  --success-bg-color: rgb(0, 206, 0);
  --error-color: rgb(136, 91, 8);
  --error-bg-color: rgb(245, 183, 68);
  max-width: 450px;
}

.alert-body {
  font-family: "Fira Code", Helvetica;
  font-size: 14px;
  font-weight: bold;
  padding: 10px;
}

.alert-type-success {
  border: 1px solid var(--success-color);
  color: var(--success-color);
  background-color: var(--success-bg-color);
}

.alert-type-error {
  border: 1px solid var(--error-color);
  color: var(--error-color);
  background-color: var(--error-bg-color);
}

.alert-text {
  /* scoped-стили всегда перебивают родительские
  - потому что они по селектору атрибута */
  text-align: left;
}

</style>
