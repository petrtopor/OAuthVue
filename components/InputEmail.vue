<template lang="pug">
  #input_email
    //- input(type='text')
    masked-input(
      type="text"
      name="phone"
      class="form-control"
      v-model="inputText"
      :mask="emailMask"
      :guide="false"
      placeholderChar="_"
      @focus="onInputFocus"
      @blur="onInputBlur"
      ref='input')
    span Введите почту, с которой отправляете письма
</template>
<style lang="scss" scoped>
div#input_email {
  display: flex;
  flex-direction: row;
  align-items: center;
  // height: 44px;
  height: 58px;
  width: 468px;
  margin-top: 27px;
  position: relative;
  // height: 64px;
  background: #ffffff;
  border: 1px solid #e0e0e0;
  box-sizing: border-box;
  border-radius: 4px;
  padding-left: 18px;

  input {
    width: 468px;
    border: none;
    /* 2018 */
    // position: absolute;
    height: 29px;
    font-family: PT Sans;
    font-style: normal;
    font-weight: normal;
    line-height: normal;
    font-size: 22px;
    color: #555555;
    outline: none;
    margin-top: 20px;
  }

  span {
    /* Введите промокод */
    position: absolute;
    width: fit-content;
    height: 24px;
    font-family: PT Sans;
    font-style: normal;
    font-weight: normal;
    line-height: normal;
    font-size: 18px;
    color: #ababab;
    // transition
    transition-property: left, top, font-size;
    transition-timing-function: ease-in-out;
    transition-duration: 0.3s;

    &.aside {
      /* Введите промокод */
      font-size: 13px;
      height: 17px;
      top: 8px;
    }
  }
}
</style>

<script>
import MaskedInput from 'vue-text-mask'
import emailMask from 'text-mask-addons/dist/emailMask'
export default {
  name: 'InputEmail',
  components: {
    MaskedInput
  },
  data() {
    return {
      testData: 'vagiz',
      selected: '',
      emailMask: emailMask,
      inputText: ''
    }
  },
  methods: {
    onInputFocus() {
      //
    },
    onInputBlur() {
      //
    }
  }
}
</script>
