<template>
  <div>
    <q-checkbox
      v-model="inputData"
      :name="name"
      :color="color"
      :label="label"
      :true-value="trueValue"
      :false-value="falseValue"
      :disable="disable || readonly"
      @update:model-value="change($event)"
      @click="onClick"
    />
  </div>
</template>

<script>
import inputMixin from '../mixins/inputMixin';
export default {
  name: 'FormBuilderCheckbox',
  mixins: [inputMixin],
  props: {
    name: {
      default: '',
      type: String,
    },
    value: {
      default: '',
      type: [Object, String, Array, Number, Boolean],
    },
    trueValue: {
      default: true,
      type: [Object, String, Array, Number, Boolean],
    },
    falseValue: {
      default: false,
      type: [Object, String, Array, Number, Boolean],
    },
  },
};
</script>

<style scoped></style>
