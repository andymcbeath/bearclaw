<template>
  <form @submit.prevent="submitForm()">
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
