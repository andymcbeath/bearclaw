# bearclaw
## Table of contents
* [General Info](#general-info)
* [Technologies](#technologies)
* [Project Setup](#project-setup)
* [Code Examples](#code-examples)
* [Final Product](#final-product)
## General Info
This is a take-home project where I had to recreate the following image:
![Bear Claw - UI Assignment 1](https://user-images.githubusercontent.com/107561577/205386853-4e7071f1-cf18-4db5-8673-d28767348bdc.png)

## Technologies
Project is created with:
* Vue version: 3.2.13
* sass version: 1.56.1
* Bootstrap version: 5.2.3

## Project Setup
In order to run this application you will need Vue version 3.2.13. cd into the project directory. You will also need the following two .png files:
/Users/amcbeath/Bearclaw/bearclaw/src/assets/never-gonna-give.png /Users/amcbeath/Bearclaw/bearclaw/src/assets/linkedin.png

npm install
run npm i bootstrap@5.2.3 and npm install sass-loader sass webpack --save-dev.

## Code Examples
Below is the UserForm code for the bottom half of the page
```
<template>
  <form id="submit" @submit.prevent="submitForm()">
    <div class="row">
      <div class="col">
        <div class="mb-3">
          <label
            type="text"
            for="formGroupExampleInput"
            class="form-label"
            style="align-content: left"
            >First Name</label
          >
          <input
            v-bind="form.firstName"
            type="text"
            class="form-control"
            id="formGroupExampleInput"
            placeholder="First Name"
          />
        </div>
        <div class="mb-3">
          <label for="formGroupExampleInput2" class="form-label"
            >Last Name</label
          >
          <input
            type="text"
            class="form-control"
            id="formGroupExampleInput2"
            placeholder="Last Name"
          />
        </div>
        <div class="mb-3">
          <label for="formGroupExampleInput" class="form-label">Title</label>
          <input
            type="text"
            class="form-control"
            id="formGroupExampleInput"
            placeholder="Title"
          />
        </div>
        <div class="mb-3">
          <label for="formGroupExampleInput2" class="form-label">Role</label>
          <input
            type="text"
            class="form-control"
            id="formGroupExampleInput2"
            placeholder="Role"
          />
        </div>
      </div>
      <div class="col-4">
        <div class="mb-3">
          <label for="formGroupExampleInput" class="form-label">Email</label>
          <input
            type="email"
            class="form-control"
            id="Email"
            placeholder="Enter a valid Email"
          />
        </div>
        <div class="mb-3">
          <label for="formGroupExampleInput2" class="form-label">Phone</label>
          <input
            type="phone"
            class="form-control"
            id="Phone"
            placeholder="Enter phone"
          />
        </div>
        <div class="mb-3">
          <label for="formGroupExampleInput" class="form-label">Password</label>
          <input
            type="password"
            class="form-control"
            id="Password"
            placeholder="Enter your password"
          />
        </div>
        <div class="mb-3">
          <label for="formGroupExampleInput2" class="form-label"
            >Default Note Action</label
          >
          <input
            type="text"
            class="form-control"
            id="Default Note Action"
            placeholder="Client Submission"
          />
        </div>
        <div class="mb-3">
          <label for="formGroupExampleInput2" class="form-label"
            >Default Landing Page upon Login</label
          >
          <input
            type="text"
            class="form-control"
            id="Default Landiing Page upon Login"
            placeholder="Dashboard"
          />
        </div>
      </div>
      <div id="buttons" class="col-4">
        <div class="d-grid mw-100 gap-2 mr-2 d-md-block">
          <h6>Alert Types</h6>
          <button type="button" class="btn btn-outline-light">Tasks</button>
          <button type="button" class="btn btn-outline-light">
            Appointments
          </button>
          <button type="button" class="btn btn-outline-light">Notes</button>
          <button
            type="button"
            class="btn btn-outline-light"
            style="margin-right: 4%"
          >
            Leads
          </button>
          <br />
          <button type="button" class="btn btn-outline-light">
            Candidates
          </button>
          <button type="button" class="btn btn-outline-light bg-blue">
            Contacts
          </button>
          <button type="button" class="btn btn-outline-light">Companies</button>
          <br />
          <button
            type="button"
            class="btn btn-outline-light"
            style="width: 100%"
          >
            Submissions
          </button>
          <h6>Delivery Methods</h6>
          <button
            type="button"
            class="btn btn-outline-light"
            style="width: 50%"
          >
            Email
          </button>
          <button
            type="button"
            class="btn btn-outline-light"
            style="width: 50%"
          >
            Slack
          </button>
        </div>
        <div class-name="last-options">
          <p>SMS (contact us to enable this method)</p>
          <br />
          <p>MS Teams (contact us to enable this method)</p>
          <br />
          <p>Zoom (contact us to enable this method)</p>
          <br />
        </div>
      </div>
    </div>
  </form>
</template>
<script>
export default {
  name: "UserForm",
  data() {
    return {
      form: { firstName: String, lastName: String },
    };
  },
  methods: {
    submitForm() {
      console.log("I am submitting this!");
    },
  },
};
</script>

<style lang="scss">
.row {
  padding-left: 100px;
  padding-right: 50px;
}
.buttons {
  justify-content: space-between;
}
#buttons {
  justify-content: space-between;
}
input[type="text"],
input[type="email"],
input[type="phone"],
input[type="password"],
textarea {
  background-color: #d1d1d1;
}
input {
  border-radius: 0.1rem;
}
</style>

```
Here is the code for the top section of the page:
```
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
              <h5>LIGHT</h5>
              <label class="switch">
                <input type="checkbox" />
                <span class="slider round"></span>
              </label>
              <h5>DARK</h5>
            </div>
            <div class="col-3">
              <h5>STABLE</h5>
              <label class="switch">
                <input type="checkbox" @click="toggleCheckbox" />
                <div class="slider round"></div>
              </label>
              <h5>BETA</h5>
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
  padding-left: 100px;
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
h5 {
  color: white;
}
</style>

```
### Final Product!
![Screenshot 2022-12-02 at 3 32 02 PM](https://user-images.githubusercontent.com/107561577/205392133-69e03295-55e8-4794-964c-d6b52ec0ce0d.png)


### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
