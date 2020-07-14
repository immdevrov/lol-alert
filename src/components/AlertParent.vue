<template>
  <div v-if="isShown" class="alert-wrapper">
    <div class="alert-body" :class="`alert-type-${type}`">
      <slot name="prepend"></slot>
      <div class="alert-text">{{ text }}</div>
      <slot name="append"></slot>
    </div>
  </div>
</template>
<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

@Component
export default class Alert extends Vue {
  @Prop({ type: String, default: '' }) text!: string
  @Prop({ type: Boolean, default: false }) isShown!: boolean
  @Prop({ type: String, default: '' }) type!: string
}

</script>

<style>
/* родительские стили. могут быть перезаписаны.
имеет смысл описывать тут reset-стили */
.alert-body {
  width: 100%;
  display: flex;
  align-items: center;
}

.alert-text {
  width: 100%;
  text-align: center;
}

</style>
