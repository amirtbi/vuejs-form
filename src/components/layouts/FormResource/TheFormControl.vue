<template>
  <div class="contact-container__form">
    <form class="form-control">
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
          <label for="lastname">Lastname</label>
          <input type="text" id="lastname" name="lastname" />
        </div>
      </div>
    </form>
  </div>
</template>

<script>
export default {};
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
div.form-row{
    display: flex;
    flex-direction: row;
    width: 100%;
    justify-content: space-between;
    align-items: center;
}
div.form-row__field{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    width:100%;
    padding:1.2rem;
}
div.form-row__field input{
    width:100%;
    border:none;
    outline:none;
    padding: 0.2rem;
    border-bottom:2px solid #cccc;
    border-radius: 2px;
    transition:all ease-in-out 0.5s;
    font-size: 1.1rem;
    font-family: inherit;
    font-weight: bold;


}
div.form-row__field input:focus{
    border-bottom:2px solid var(--primaryColor);
}
div.form-row__field label{
    font-family: inherit;
    filter:opacity(0.5);
}
</style>
