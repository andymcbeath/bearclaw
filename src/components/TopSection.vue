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
              >
                Submit Changes
              </button>
            </div>
            <div class="col-3">
              <h6>LIGHT</h6>
              <div class="form-check form-switch">
                <input
                  class="form-check-input"
                  type="checkbox"
                  role="switch"
                  id="flexSwitchCheckChecked"
                  checked
                />
                <label class="form-check-label" for="flexSwitchCheckChecked"
                  >DARK</label
                >
              </div>
            </div>
            <div class="col-3">
              <h6>STABLE</h6>
              <div class="form-check form-switch">
                <input
                  class="form-check-input"
                  type="checkbox"
                  role="switch"
                  id="flexSwitchCheckChecked"
                  checked
                />
                <label class="form-check-label" for="flexSwitchCheckChecked"
                  >BETA</label
                >
              </div>
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
.buttons:after {
  content: "";
  display: inline-block;
  width: 99.5%; /* generates an extra transparent line */
}
.middle-top {
  display: flex;
}
.buttons {
  min-width: 45em;
  padding: 1.2em 1em 0;
  box-shadow: 0 0 5px;
  margin: 1em;
  border-radius: 0.25em;
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
.buttons:after {
  content: "";
  display: inline-block;
  width: 99.5%; /* generates an extra transparent line */
}
</style>
