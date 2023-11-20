<script setup>
import { ref } from "vue";

// reactive state
const isActive = ref(false);

// functions that mutate state and trigger updates
const toggleWindow = () => {
  isActive.value = !isActive.value;
};
</script>

<template>
  <div>
    <div class="centered">
      <div
        :class="{ 'plus--active': isActive }"
        @click="toggleWindow"
        id="plus"
      >
        <div class="plus__line plus__line--v">
          <div class="container">
            <div class="close">close</div>
            <form id="contact" action="" method="post">
              <h3>Customer registration</h3>
              <h4>Balek lat9la6 vchi</h4>
              <fieldset>
                <input
                  placeholder="Client name"
                  type="text"
                  tabindex="1"
                  required
                  autofocus
                />
              </fieldset>
              <fieldset>
                <input
                  placeholder="Client code"
                  type="text"
                  tabindex="2"
                  required
                />
              </fieldset>
              <fieldset>
                <input
                  placeholder="Client Phone Number (optional)"
                  type="tel"
                  tabindex="3"
                  required
                />
              </fieldset>

              <fieldset>
                <button
                  name="submit"
                  type="submit"
                  id="contact-submit"
                  data-submit="...Sending"
                >
                  Submit
                </button>
              </fieldset>
            </form>
          </div>
        </div>
        <div class="plus__line plus__line--h"></div>
      </div>
    </div>
  </div>
</template>
<style scoped>
#plus {
  width: 60px;

  transition: all 0.3s ease 0s;
  height: 60px;
  background: #4dc3fa;
  border-radius: 50%;
  display: flex;
  /* position: relative; */
  position: fixed;
  left: 80%;
  top: 88%;
}
.plus__line {
  width: 6px;
  height: 50px;
  background: #323c50;
  border-radius: 10px;
  position: absolute;
  left: calc(50% - 3px);
  top: calc(50% - 25px);
}
.plus__line--h {
  transform: rotate(90deg);
}
.plus__line--v {
  display: flex;
  align-items: center;
  justify-content: space-around;
  overflow: hidden;
  transition: all 0.4s ease 0s;
}
.plus__link {
  color: #fff;
  font-size: 30px;
  opacity: 0;
  visibility: hidden;
  transition: 0.3s ease 0s;
  transform: scale(0.5);
}
.plus--active {
  height: 32px;
  border-radius: 30px;
}
.plus--active .plus__line--v {
  transform: translate(-50%, -50%);
  height: 100vh;
  top: 50%;
  padding: 0 5px;
  box-sizing: border-box;
  width: 100vw;
  /* border-radius: 60px;
	 */
  left: 50%;
  position: fixed;
}
.plus--active .plus__link {
  opacity: 1;
  visibility: visible;
  transform: scale(1);
  transition-delay: 0.05s;
}

.close {
  position: absolute;
  top: 5%;
  left: 84%;
}

.container {
  max-width: 400px;
  width: 100%;
  margin: 0 auto;
  position: relative;
}

#contact input[type="text"],
#contact input[type="email"],
#contact input[type="tel"],
#contact input[type="url"],
#contact textarea,
#contact button[type="submit"] {
  font: 400 12px/16px "Roboto", Helvetica, Arial, sans-serif;
}

#contact {
  background: #323c50;
  padding: 25px;
  margin: 150px 0;
}

#contact h3 {
  display: block;
  font-size: 30px;
  font-weight: 300;
  margin-bottom: 10px;
}

#contact h4 {
  margin: 5px 0 15px;
  display: block;
  font-size: 13px;
  font-weight: 400;
}

fieldset {
  border: medium none !important;
  margin: 0 0 10px;
  min-width: 100%;
  padding: 0;
  width: 100%;
}

#contact input[type="text"],
#contact input[type="email"],
#contact input[type="tel"],
#contact textarea {
  width: 100%;
  border: 1px solid #ccc;
  background: #1f2739;
  margin: 0 0 5px;
  padding: 10px;
}

#contact input[type="text"]:hover,
#contact input[type="email"]:hover,
#contact input[type="tel"]:hover,
#contact textarea:hover {
  -webkit-transition: border-color 0.3s ease-in-out;
  -moz-transition: border-color 0.3s ease-in-out;
  transition: border-color 0.3s ease-in-out;
  border: 1px solid #aaa;
}

#contact textarea {
  height: 100px;
  max-width: 100%;
  resize: none;
}

#contact button[type="submit"] {
  width: 100%;
  border: none;
  background: #4dc3fa;
  color: #fff;
  margin: 25px 10px 25px;
  padding: 10px;
  font-size: 15px;
  border-radius: 25px;
}

#contact button[type="submit"]:hover {
  background: #43a047;

  transition: background-color 0.3s ease-in-out;
}

#contact button[type="submit"]:active {
  box-shadow: inset 0 1px 3px rgba(0, 0, 0, 0.5);
}

.copyright {
  text-align: center;
}

#contact input:focus,
#contact textarea:focus {
  outline: 0;
  border: 1px solid #aaa;
}

::-webkit-input-placeholder {
  color: #888;
}

:-moz-placeholder {
  color: #888;
}

::-moz-placeholder {
  color: #888;
}

:-ms-input-placeholder {
  color: #888;
}
</style>
