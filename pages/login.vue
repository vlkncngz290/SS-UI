<template>
  <div class="container">
    <div class="row justify-content-center">
      <div class="col-md-9 col-lg-12 col-xl-10">
        <div class="card shadow-lg o-hidden border-0 my-5">
          <div class="card-body p-0">
            <div class="row">
              <div class="col-lg-6 col-xxl-12">
                <div class="p-5">
                  <div class="text-center">
                    <h4 class="text-dark mb-4">Login</h4>
                  </div>

                  <div class="mb-3"><input v-model="username" id="exampleInputEmail" class="form-control form-control-user" type="email"
                                           aria-describedby="emailHelp" placeholder="Username"
                                           name="email"/></div>
                  <div class="mb-3"><input v-model="password" id="exampleInputPassword" class="form-control form-control-user"
                                           type="password" placeholder="Password" name="password"/></div>
                  <div class="mb-3">
                    <div class="custom-control custom-checkbox small">
                      <div class="form-check"><input id="formCheck-1" class="form-check-input custom-control-input"
                                                     type="checkbox"/><label
                        class="form-check-label custom-control-label" for="formCheck-1">Remember Me</label></div>
                    </div>
                  </div>
                  <button class="btn btn-primary d-block btn-user w-100" type="submit" @click="login">Login
                  </button>
                  <hr/>

                  <div class="text-center"></div>
                  <div class="text-center"></div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "login",
  data() {
    return{
      username: "",
      password: ""
    }
  },
  methods: {
    async login() {
      let data={
        mail:this.username,
        password:this.password
      }
      let res=await this.$axios.post('login',data)
      console.log(res.data.token)
      this.$axios.setHeader('Token',res.data.token)
      this.$router.push("/")
    },
    returnHome(){
      this.$router.push("/")
    }
  }
}
</script>

<style scoped>

</style>
