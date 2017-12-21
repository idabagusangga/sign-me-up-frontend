<template lang="html">
  <div class="container">
      <h3></h3>
      <div class="form-group">
        <label for="exampleInputEmail1">Email address</label>
        <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Enter email">
      </div>
      <div class="form-group">
        <label for="exampleInputPassword1">Password</label>
        <input type="password" class="form-control" id="exampleInputPassword1" placeholder="Password">
      </div>
  </div>
</template>

<script>
export default {
    data(){
        return{
            msg:'Welcome to Sign Me Up',
            errorMsg:""
            
        }
    },
    methods : {
        login(){
            axios.post('/',{
                email : req.body.email,
                password : req.body.password
            })
            .then(response=>{
                 localStorage.setItem("token",response.token)
                 
            })
            .catch(err=>{
                this.errorMsg = err
            })
        }
    }
}
</script>

<style lang="css">
</style>
