<template>
  <div class="p-4 border w-100 mb-4" id="user">


  </div>

</template>

<script>
import axios from 'axios';
export default {
  data() {
    return {


    }
  },
  methods: {
    async createUser() {
      const user = { Name : this.user_name, Country: this.Country, Email: this.email, Password: this.password };
      console.log(user);
      await axios.post("https://localhost:44342/api/User", user);
    }
  },
  mounted() {
  }

}
</script>

<style>
*{
  padding: 4px;
}

.border{
  border: solid black 1px;
}
</style>
