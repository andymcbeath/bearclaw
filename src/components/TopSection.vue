<template>
  <ProjectInfo
    title="TopSection"
    :contributor="{ name: 'Andy McBeath', email: 'mcbeath1@gmail.com' }"
    description="This is the top of the page"
  />
  <div class="container-flex">
    <div class="row">
      <div class="col-3">
        <div class="picture">
          <img
            src="@/assets/never-gonna-give.png"
            class="img-thumbnail"
            alt="..."
          />
        </div>
      </div>
      <div id="middle-top" class="col-6">
        <div class="edit-user">
          <h1>Edit User</h1>
        </div>
        <br />
        <div class="middle-top">
          <div class="row">
            <div class="col-6">
              <button
                type="button"
                class="btn btn-outline-green"
                style="background-color: green"
                form="submit"
              >
                Submit Changes
              </button>
            </div>
            <div class="col-3">
              <h6>LIGHT</h6>
              <label class="switch">
                <input type="checkbox" />
                <span class="slider round"></span>
              </label>
              <h6>DARK</h6>
            </div>
            <div class="col-3">
              <h6>STABLE</h6>
              <label class="switch">
                <input type="checkbox" @click="toggleCheckbox" />
                <div class="slider round"></div>
              </label>
              <h6>BETA</h6>
            </div>
          </div>
        </div>
      </div>
      <div class="col-3">
        <button type="button" width="30" class="btn btn-primary">
          <span
            ><img
              src="../../src/assets/linkedin.png"
              class="rounded float-start"
          /></span>
          PROFILE CONNECTED
        </button>
        <br />
        <p>Re-Connect Linkedin Profile</p>
      </div>
    </div>
  </div>
  <UserForm @submit="handleSubmit()" />
</template>
<script>
import UserForm from "@/components/UserForm.vue";

export default {
  name: "TopSection",
  components: { UserForm },
};
</script>
<style class="scss">
.col-3 {
  align-items: center;
}
.buttons:after {
  content: "";
  display: inline-block;
  width: 99.5%; /* generates an extra transparent line */
}

.buttons {
  min-width: 45em;
  padding: 1.2em 1em 0;
  box-shadow: 0 0 5px;
  margin: 1em;
  border-radius: 0.25em;
}
.buttons {
  min-width: 45em;
  padding: 1.2em 1em 0;
  box-shadow: 0 0 5px;
  margin: 1em;
  border-radius: 0.25em;
}
.toggle-seperator {
  padding-left: 4%;
  padding-right: 1%;
}
img.img-thumbnail {
  border-color: #1d202e;
  border-radius: 50%;
  width: 150px;
  height: 150px;
  border-width: 15px;
  color: #1d202e;
  background-color: #1d202e;
}
.picture {
  color: #1d202e;
  background-color: #1d202e;
  border-color: #1d202e;
  color: #1d202e;
  border-radius: 50%;
  width: 150px;
  height: 150px;
}
.container-flex {
  padding-top: 100px;
}
.middle-top {
  display: flex;
}

.switch {
  font-size: 15px;
  position: relative;
  left: 10px;
  top: 2px;
  width: 3.5em;
  height: 2.1em;
}

/* Hide default HTML checkbox */
.switch input {
  opacity: 0;
  width: 0;
  height: 0;
}

/* The slider */
.slider {
  position: absolute;
  cursor: pointer;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: #f4f4f5;
  transition: 0.4s;
  border-radius: 10px;
}
.slider:before {
  position: absolute;
  content: "";
  height: 1.4em;
  width: 1.4em;
  border-radius: 20px;
  left: 0.3em;
  bottom: 0.3em;
  background: linear-gradient(40deg, #1de83b, #1de83b 70%);
  -webkit-transition: 0.4s;
  transition: 0.4s;
}

input:checked + .slider {
  background-color: #303136;
}

input:checked + .slider:before {
  transform: translateX(1.5em);
  background: lightgrey;
  background: linear-gradient(40deg, #1de83b, #1de83b 70%);
  /* box-shadow: inset -3px -2px 5px -2px #1de83b, inset -10px -5px 0 0 #1de83b; */
}

/* Rounded sliders */
.slider.round {
  border-radius: 34px;
}

.slider.round:before {
  border-radius: 50%;
}
</style>
