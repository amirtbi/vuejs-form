<template>
  <div class="contact-container__form">
    <form class="form-control" @submit.prevent>
      <!--form-row-->
      <div class="form-row">
        <div class="form-row__field">
          <label for="firstname">First Name</label>
          <input type="text" id="firstname" name="firstname" />
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
          <input type="tell" id="phone" name="phone" />
        </div>
      </div>
      <div class="form-row">
        <div class="form-row__field">
          <label for="age">Your Age</label>
          <input type="number" id="age" name="age" min="10" max="60" />
        </div>
        <div class="form-row__field">
          <label for="howHear">How Did you hear about us?</label>
          <select name="howHear" id="howHear">
            <option value="Google">Google</option>
            <option value="Facebook">Facebook</option>
            <option value="Instagram">Instagram</option>
          </select>
        </div>
      </div>
      <div class="form-row form-row--justify">
        <div class="form-row--checkbox">
          <p>What are you intrested in?</p>
          <div class="form-checkbox">
            <input type="checkbox" name="user-intrest" />
            <label for="user-intrest">News</label>
          </div>
          <div class="form-checkbox">
            <input type="checkbox" name="user-intrest" />
            <label for="user-intrest">Tutorials</label>
          </div>
          <div class="form-checkbox">
            <input type="checkbox" name="user-intrest" />
            <label for="user-intrest">Nothing</label>
          </div>
        </div>
        <div class="form-row--radiobox">
          <p>How Do You Learn?</p>
          <div class="form-radiobox">
            <input type="radio" name="user-intrest" />
            <label for="user-intrest">News</label>
          </div>
          <div class="form-radiobox">
            <input type="radio" name="user-intrest" />
            <label for="user-intrest">Tutorials</label>
          </div>
          <div class="form-radiobox">
            <input type="radio" name="user-intrest" />
            <label for="user-intrest">Nothing</label>
          </div>
        </div>
      </div>
      <div class="button-container">
        <base-button @click="displayAlert" mode="action">SUBMIT</base-button>
      </div>   
    </form>
  </div>
</template>

<script>
export default {
  methods:{
    displayAlert(){
      alert("form is submitted")
          }
  }
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
div.form-row--justify{
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
div.form-row--radiobox{
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
  width: 20%;
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
div.button-container{
    display: flex;
    flex-direction: row;
    justify-content: flex-end;
    align-content: center;
    width: 100%;
    margin-top: 1rem;
    padding: 1.2rem;
}
</style>
