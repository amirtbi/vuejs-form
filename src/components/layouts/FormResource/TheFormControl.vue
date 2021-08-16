<template>
  <div class="contact-container__form">
    <!--form -->
    <form class="form-control" @submit.prevent="showUserInput">
      <!--form-row-->
      <div class="form-row">
        <div
          class="form-row__field"
          :class="{ invalid: userNameValidity === 'invalid' }"
        >
          <label for="firstname">First Name</label>
          <input
            type="text"
            id="firstname"
            name="firstname"
            v-model.trim="userName"
            @blur="userNameValidation"
          />
          <small class="caution-message" v-if="userNameValidity === 'invalid'"
            >Please fill the blank input!</small
          >
        </div>
        <div class="form-row__field">
          <label for="lastname">Last Name</label>
          <input type="text" id="lastname" name="lastname" />
        </div>
      </div>
      <div class="form-row">
        <div class="form-row__field">
          <label for="mail">Mail</label>
          <input type="email" id="mail" name="mail" />
        </div>
        <div class="form-row__field">
          <label for="firstname">Phone</label>
          <input type="tell" id="phone" name="phone" ref="userPhone" />
        </div>
      </div>
      <div class="form-row">
        <div class="form-row__field">
          <label for="age">Your Age</label>
          <input
            type="number"
            id="age"
            name="age"
            min="10"
            max="60"
            v-model="userAge"
          />
        </div>
        <div class="form-row__field">
          <label for="howHear">How Did you hear about us?</label>
          <select name="howHear" id="howHear" v-model="referre">
            <option value="Google">Google</option>
            <option value="Facebook">Facebook</option>
            <option value="Instagram">Instagram</option>
          </select>
        </div>
      </div>
      <div>
        <rating-control
          v-model="rating"
        ></rating-control>
      </div>
      <!--user interest checkboxes-->
      <div class="form-row form-row--justify">
        <div class="form-row--checkbox">
          <p>What are you intrested in?</p>
          <div class="form-checkbox">
            <input
              type="checkbox"
              name="user-intrest"
              value="news"
              v-model="interest"
            />
            <label for="user-intrest">News</label>
          </div>
          <div class="form-checkbox">
            <input
              type="checkbox"
              name="user-intrest"
              value="tutorial"
              v-model="interest"
            />
            <label for="user-intrest">Tutorials</label>
          </div>
          <div class="form-checkbox">
            <input
              type="checkbox"
              name="user-intrest"
              value="nothing"
              v-model="interest"
            />
            <label for="user-intrest">Nothing</label>
          </div>
        </div>
        <!--user how learn radiobuttons -->
        <div class="form-row--radiobox">
          <p>How Do You Learn?</p>
          <div class="form-radiobox">
            <input
              type="radio"
              name="learning-how"
              v-model="how"
              value="Video course"
            />
            <label for="user-intrest">Video Courses</label>
          </div>
          <div class="form-radiobox">
            <input
              type="radio"
              name="learning-how"
              v-model="how"
              value="Blogs"
            />
            <label for="user-intrest">Blogs</label>
          </div>
          <div class="form-radiobox">
            <input
              type="radio"
              name="learning-how"
              v-model="how"
              value="Other"
            />
            <label for="user-intrest">Other</label>
          </div>
        </div>
      </div>

      <div class="button-container">
        <div class="confirm-container">
          <input
            type="checkbox"
            id="confirmed-terms"
            name="confirmed-terms"
            v-model="confirmed"
          />
          <label for="confirmed-terms">Do you agree all terms?</label>
        </div>
        <base-button mode="action">SUBMIT</base-button>
      </div>
    </form>
  </div>
</template>

<script>
import RatingControl from "./RatingControl.vue";
export default {
  components: {
    RatingControl,
  },
  data() {
    return {
      userName: "",
      userAge: null,
      referre: "Google",
      interest: [],
      how: null,
      confirmed: false,
      rating: null,
      userNameValidity: "pending",
    };
  },

  methods: {
    showUserInput() {
      console.log("username:" + this.userName);
      console.log("user Age :" + this.userAge);
      //show type of this.$refs
      console.log("user phone number :" + typeof this.$refs.userPhone.value);
      this.userName = "";
      console.log("referre :" + this.referre);
      this.referre = "Google";
      console.log("User interest :");
      console.log("=======");
      for (let intr of this.interest) {
        console.log(intr);
      }

      console.log("=======");
      //reseting the checkboxes
      this.interest = [];

      console.log("user learning approach:");
      console.log(this.how);

      //reseting radioboxes
      this.how = null;
      //show true/false checkbox
      console.log(this.confirmed);
      this.confirmed = false;
      //show rating
      console.log("rating :" + this.rating);
      this.rating = null;
    },
    userNameValidation() {
      if (this.userName === "") {
        this.userNameValidity = "invalid";
      } else {
        this.userNameValidity = "valid";
      }
    },
   
  },
};
</script>

<style scoped>
div.contact-container__form {
  width: 100%;
}
form.control {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  width: 100%;
}
div.form-row {
  display: flex;
  flex-direction: row;
  width: 100%;
  justify-content: space-between;
  align-items: center;
}

div.form-row--justify {
  justify-content: flex-start;
}
div.form-row__field {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  width: 100%;
  padding: 1.2rem;
}
div.form-row__field input {
  width: 100%;
  border: none;
  outline: none;
  padding: 0.2rem;
  border-bottom: 2px solid #cccc;
  border-radius: 2px;
  transition: all ease-in-out 0.5s;
  font-size: 1.1rem;
  font-family: inherit;
  font-weight: bold;
}
div.form-row__field input:focus {
  border-bottom: 2px solid var(--primaryColor);
}
div.form-row__field label {
  font-family: inherit;
  filter: opacity(0.5);
}
div.form-row__field.invalid input {
  border-bottom: 2px solid red;
}
div.form-row__field.invalid label {
  color: red;
}

small.caution-message {
  color: red;
}
select {
  width: 70%;
  padding: 0.5rem;
  margin-top: 0.5rem;
  font-family: inherit;
  font-weight: bold;
  color: black;
  border: 2px solid rgba(180, 179, 179, 0.8);
  outline: none;
}
div.form-row--radiobox {
  margin-left: 5rem;
}
div.form-row--checkbox,
div.form-row--radiobox {
  flex-direction: column;
}
div.form-row--checkbox p,
div.form-row--radiobox p {
  margin: 0;
  padding: 0.2rem 1.2rem;
  font-family: inherit;
  font-weight: bold;
}
div.form-checkbox,
div.form-radiobox {
  display: flex;
  flex-direction: row;
  width: 100%;
  justify-content: flex-start;
  align-content: center;
  padding: 0.2rem 1.2rem;
}
div.form-checkbox label,
div.form-radiobox label {
  font-family: inherit;
  font-weight: bold;
  margin-left: 0.2rem;
}
div.button-container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-content: center;
  width: 100%;
  margin-top: 1rem;
  padding: 1.2rem;
}
div.confirm-container {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
div.confirm-container label {
  font-weight: bold;
  font-family: inherit;
  margin-left: 0.2rem;
}
</style>
