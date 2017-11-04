<template lang="html">
  <div class="container">
  	<div class="login">
  		<h4>Login to Web App</h4>
  			<hr>
          		<form class="login-inner">
      				<input type="email" v-model="email" class="form-control email" id="email-input" placeholder="Enter email">
      				<input type="password" v-model="password" class="form-control password" id="password-input" placeholder="Password">
  					<label class="checkbox-inline">
  						<input type="checkbox" id="remember" value="Remember me"> Remember me
  					</label>
  					<input @click="login" class="btn btn-block btn-lg btn-success submit" type="submit" value="Login">
  				</form>
  			<a href="#" class="btn btn-sm btn-primary register">Register</a>
  			<a href="#" class="btn btn-sm btn-default forgot">Forgot your password?</a>
  	</div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      email: '',
      password: ''
    }
  },
  methods:{
    login(){
      var data = {
        client_id: 2,
        client_secret: '2GmVX6VkB21vai8w4ToLozECqFOvy0IotWLvZqQs',
        grant_type: 'password',
        username: this.email,
        password: this.password
      }
      this.$http.post("oauth/token",data)
        .then(response => {
          this.$auth.setToken(response.body.access_token,response.body.expires_in + Date.now())

          this.$router.push("/feed")
        })
    }
  }
}
</script>

<style lang="css">

</style>
