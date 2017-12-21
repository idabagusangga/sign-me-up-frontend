<template lang="html">
  <div class="container">
      <h1>{{msg}}</h1>
      <div class="container">
          <div class="form-group">
              <label class="col-form-label" for="inputDefault">Email</label>
              <input type="text" class="form-control" placeholder="Default input" id="inputDefault">
          </div>
          <div class="form-group">
              <label class="col-form-label" for="inputDefault">Password</label>
              <input type="text" class="form-control" placeholder="Default input" id="inputDefault">
          </div>
          <input type="submit" name="" value="Login">
      </div>
  </div>
</template>

<script>
export default {
    data(){
        return{
            msg:'Welcome to Sign Me Up'
        }
    }
}
</script>

<style lang="css">
</style>
