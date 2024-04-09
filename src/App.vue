<script>
import welcome from "./welcoming/components/welcome.component.vue";
import ShowDeveloperCount from "./welcoming/components/show-developer-count.component.vue";


export default
{
  name: "app",
  components:{ShowDeveloperCount, welcome},
  data()
  {
    return{
      firstName: 'Julio',
      lastName: 'Elsner',
      developerCount: 0
    }
  },
  methods:
      {
        onDeveloperRegistered(developer)
        {
          this.firstName = developer.firstName;
          this.lastName = developer.lastName;
          console.log("Developer registered:", developer);
          this.updateDeveloperCount(developer);
        },

        updateDeveloperCount(developer)
        {
          if (developer.fullName !== "Unknown")
          {
            this.developerCount++;
          }
        }
      }
}


</script>

<template>
  <h1>Hello Vue Developer Application</h1>
  < v-on: developer-registered = "onDeveloperRegistered"/>
  <welcome :first-name= "firstName" :last-name= "LastName"/>
  <show-developer-count :developer-count = "developerCount"/>
</template>