<script>
export default
{
  name: "register-developer",
  data()
  {
    return {
      firstName: '',
      lastName: '',
    }
  },
  methods:
      {
        onsubmit()
        {
          console.log("Registering Developer");
          this.$emit("developer-registered",{
            firstName: this.firstName,
            lastName: this.lastName
          });
        }
      }
}
</script>

<template>

  <div>
    <h2>
      <form @submit.prevent="onsubmit">
        <div>
          <label for = "firstName">First Name</label>
          <input type="text" name="firstName" v-model="firstName" required>
        </div>
        <div>
          <label for = "lastName">Last Name</label>
          <input type="text" name="lastName" v-model="lastName" required>
        </div>
        <div>
          <button type="submit"> Register </button>
        </div>
      </form>
    </h2>




  </div>

</template>

<style scoped>

</style>