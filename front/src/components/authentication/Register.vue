<template lang="html">
  <div class="container">
  	<div class="register">
  		<h4>Register to Web App</h4>
  			<hr>
          		<form class="register-inner">
              <input type="text" v-model="name" class="form-control name" id="name-input" placeholder="Enter name">
      				<input type="email" v-model="email" class="form-control email" id="email-input" placeholder="Enter email">
      				<input type="password" v-model="password" class="form-control password" id="password-input" placeholder="Password">
  					<label class="checkbox-inline">
  						<input type="checkbox" id="remember" value="Remember me"> Remember me
  					</label>
  				</form>
          <input class="btn btn-block btn-lg btn-success submit" type="submit" value="Register">
  			<a href="#" class="btn btn-sm btn-primary register">Login</a>
  			<a href="#" class="btn btn-sm btn-default forgot">Forgot your password?</a>
  	</div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      name: '',
      email: '',
      password: ''
    }
  }
}
</script>

<style lang="css">

</style>
