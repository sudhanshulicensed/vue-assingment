<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <TestAgain></TestAgain>
    <ConsoleLogs></ConsoleLogs>
    <Time-Check></Time-Check>
    <CheckBox></CheckBox>
    <DropDown></DropDown>
    <ArrDropDown></ArrDropDown>
  </div>
</template>

<script>
import TestAgain from './components/Test.vue'

import ConsoleLogs from './components/ConsoleLog.vue'

import TimeCheck from "./components/Time.vue"

import CheckBox from "./components/Checkbox.vue"

import DropDown from "./components/Dropdown.vue"

import ArrDropDown from "./components/DropDownArray.vue"

export default {
  name: 'App',
  components: {
  TestAgain,
  ConsoleLogs,
  TimeCheck,
  CheckBox,
  DropDown,
  ArrDropDown
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
