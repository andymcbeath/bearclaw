<template>
  <ProjectInfo
    title="TopSection"
    :contributor="{ name: 'Andy McBeath', email: 'mcbeath1@gmail.com' }"
    description="This is the top of the page"
  />
  <div class="container-flex">
    <div class="row">
      <div class="col-4">
        <div class="picture">
          <img
            src="@/assets/never-gonna-give.png"
            class="img-thumbnail"
            alt="..."
          />
        </div>
      </div>
      <div class="col-4">
        <div class="edit-user">
          <h1>Edit User</h1>
        </div>
        <br />
        <div class="middle-top">
          <button
            type="button"
            class="btn btn-outline-green"
            style="background-color: green"
          >
            Submit Changes
          </button>
          <h6>LIGHT</h6>
          <label class="switch">
            <input type="checkbox" onchange="darkMode()" />
            <span class="slider round"></span>
          </label>
          <h6>DARK</h6>
          <h6>STABLE</h6>
          <label class="switch">
            <input type="checkbox" @click="toggleCheckbox" />
            <div class="slider round"></div>
          </label>
          <h6>BETA</h6>
        </div>
      </div>
      <div class="col-4">
        <button type="button" class="btn btn-outline-primary">
          <span
            ><img
              src="../../src/assets/linkedin.png"
              class="rounded float-start"
          /></span>
          PROFILE CONNECTED
        </button>
        <div></div>
        Re-Connect Linkedin Profile
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TopSection",
};
</script>
