<script setup></script>

<template>
  <div>
    <input type="checkbox" id="switch" /><label for="switch">Toggle</label>
  </div>
</template>

<style scoped>
input[type="checkbox"] {
  height: 0;
  width: 0;
  visibility: hidden;
}
label {
  text-indent: -99px;
  width: 58px;
  height: 30px;
  background: #323c50;
  display: block;
  border-radius: 100px;
  position: relative;
}
label:after {
  content: "";
  position: absolute;
  top: 5px;
  left: 5px;
  width: 20px;
  height: 20px;
  background: #4dc3fa;
  border-radius: 90px;
  transition: 0.3s;
}
input:checked + label {
  background: #fff842;
}
input:checked + label:after {
  left: calc(100% - 10px);
  transform: translateX(-100%);
}
label:active:after {
  width: 50px;
}
</style>
