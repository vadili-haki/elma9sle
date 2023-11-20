<script setup>
import AddClient from "./components/AddClient.vue";
import Toggle from "./components/Toggle.vue";
</script>

<template>
  <div>
    <Toggle />

    <h1><span class="blue">&lt;</span>Goat<span class="blue">&gt;</span></h1>

    <div class="box">
      <div class="container-3">
        <span class="icon">
          <img
            style="max-width: 30px"
            src="../public/system-regular-42-search.gif"
            alt=""
          />
        </span>
        <input type="search" id="search" placeholder="Search..." />
      </div>
    </div>

    <table class="container">
      <thead>
        <tr>
          <th><h1>name</h1></th>
          <th><h1>phone N°</h1></th>
          <th><h1>code</h1></th>
        </tr>
      </thead>
      <tbody>
        <tr v-for=" i in 25">
          <td>Google</td>
          <td>44521689</td>
          <td>6369</td>
        </tr>
    
        

      </tbody>
    </table>
    <AddClient />
  </div>
</template>

<style scoped>
.blue {
  color: #185875;
}
.yellow {
  color: #fff842;
}

.container th h1 {
  font-weight: bold;
  font-size: 1em;
  text-align: left;
  color: #185875;
}

.container td {
  font-weight: normal;
  font-size: 1em;
  -webkit-box-shadow: 0 2px 2px -2px #0e1119;
  -moz-box-shadow: 0 2px 2px -2px #0e1119;
  box-shadow: 0 2px 2px -2px #0e1119;
}

.container {
  text-align: left;
  overflow: hidden;
  width: 100%;
  margin: 0 auto;
  display: table;
  padding: 0 0 8em 0;
}

.container td,
.container th {
  padding-bottom: 2%;
  padding-top: 2%;
  padding-left: 2%;
}

/* Background-color of the odd rows */
.container tr:nth-child(odd) {
  background-color: #323c50;
}

/* Background-color of the even rows */
.container tr:nth-child(even) {
  background-color: #2c3446;
}

.container th {
  background-color: #1f2739;
}

.container td:first-child {
  color: #fb667a;
}

.container tr:hover {
  background-color: #464a52;
  -webkit-box-shadow: 0 6px 6px -6px #0e1119;
  -moz-box-shadow: 0 6px 6px -6px #0e1119;
  box-shadow: 0 6px 6px -6px #0e1119;
}

.container td:hover {
  background-color: #fff842;
  color: #403e10;
  font-weight: bold;

  box-shadow: #7f7c21 -1px 1px, #7f7c21 -2px 2px, #7f7c21 -3px 3px,
    #7f7c21 -4px 4px, #7f7c21 -5px 5px, #7f7c21 -6px 6px;
  transform: translate3d(6px, -6px, 0);

  transition-delay: 0s;
  transition-duration: 0.4s;
  transition-property: all;
  transition-timing-function: line;
}

@media (max-width: 800px) {
  .container td:nth-child(4),
  .container th:nth-child(4) {
    display: none;
  }
}

/* search */

.box {
  margin: 40px auto;
  width: 300px;
  height: 1px;
}

.container-3 {
  width: 300px;
  vertical-align: middle;
  white-space: nowrap;
  position: relative;
}

.container-3 input#search {
  width: 300px;
  height: 50px;
  background: #323c50;
  border: none;
  font-size: 10pt;
  float: left;
  color: #262626;
  padding-left: 62px;
  -webkit-border-radius: 25px;
  -moz-border-radius: 25px;
  border-radius: 25px;
  color: #a7a1a6;
  margin-bottom: 40px;
}

.container-3 input#search::-webkit-input-placeholder {
  color: #65737e;
}

.container-3 input#search:-moz-placeholder {
  /* Firefox 18- */
  color: #65737e;
}

.container-3 input#search::-moz-placeholder {
  /* Firefox 19+ */
  color: #65737e;
}

.container-3 input#search:-ms-input-placeholder {
  color: #65737e;
}

.container-3 .icon {
  position: absolute;

  margin-left: 10px;
  margin-top: 10px;

  -webkit-transition: all 0.55s ease;
  -moz-transition: all 0.55s ease;
  -ms-transition: all 0.55s ease;
  -o-transition: all 0.55s ease;
  transition: all 0.55s ease;
  background: #185875;
  display: flex;
  justify-content: center;
  border-radius: 50%;
  width: 30px;
  height: 30px;
}
</style>
