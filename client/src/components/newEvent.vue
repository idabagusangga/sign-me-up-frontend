<template lang="html">
  <div class="">
      <h3 v-if="!status">{{msg}}</h3>
      <form class="" @submit="createAcara" >
          <div class="form-group container">
              <label for="exampleInputEmail1">Name</label>
              <input type="text" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Enter email">
              <small id="emailHelp" class="form-text text-muted">We'll never share your email with anyone else.</small>
          </div>
          <div class="form-group container">
              <label for="exampleInputEmail1">Starting Date</label>
              <input type="date" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Enter email">
              <small id="emailHelp" class="form-text text-muted">We'll never share your email with anyone else.</small>
          </div>
          <div class="form-group container">
              <label for="exampleInputFile">File input</label>
              <input type="file" name="logoEvent" class="form-control-file" id="exampleInputFile" aria-describedby="fileHelp">
              <small id="fileHelp" class="form-text text-muted">Please input your event logo</small>
          </div>
          <div class="form-group container">
              <label for="exampleTextarea">Example textarea</label>
              <textarea class="form-control" id="exampleTextarea" rows="3"></textarea>
          </div>
          <input type="submit" value="Create">
      </form>
      
    </div>
</template>

<script>
export default {
    data(){
        return{
            msg:"Please Log In",
            status:true
        }
    },
    methods : {
        createAcara(){
            // let token = localStorage.getItem('token')
            // let acaraBaru = {
            //     name: "",
            //     startDate : "",
            //     logoEvent : "",
            //     description : ""
            //     
            // }
            // let options = {
            //     headers: {
            //         Authorization : "Bearer " + token
            //     }
            // }
            // axios.post('http://localhost:3000/api/events',acaraBaru,options)
            this.$router.push('/guest')
        }
    }
}
</script>

<style lang="css">
</style>
