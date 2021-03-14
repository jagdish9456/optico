<template>
<section class="ftco-section">
  <div class="container">
    <div class="row justify-content-center">
      <div class="col-md-12 col-lg-10">
        <div class="wrap d-md-flex">
          <div class="img">
              <img src="../assets/bg.png">
          </div>
          <div class="login-wrap p-md-5" style="padding-top:20%">
            <div class="d-flex">
              <div class="w-100">
                <h3 class="mb-4">Login to Dashboard</h3>
              </div>
            </div>
            <form action="#" class="signin-form">
              <div class="form-group mb-3">
                <label class="label" for="name">Username</label>
                <input
                  type="text"
                  class="form-control"
                  placeholder="Username"
                  required=""
                />
              </div>
              <div class="form-group mb-3">
                <label class="label" for="password">Password</label>
                <input
                  type="password"
                  class="form-control"
                  placeholder="Password"
                  required=""
                />
              </div>
              <div class="form-group d-md-flex">
                <div class="w-100 text-left">
                  <label class="checkbox-wrap checkbox-primary mb-0"
                    >Remember Me
                    <input type="checkbox" checked="" />
                    <span class="checkmark"></span>
                  </label>
                </div>
              </div>
              <div class="form-group">
                
              </div>
              <div class="form-group d-md-flex">
                <div class="w-50 text-left">
                 <button
                  type="submit"
                  class="form-control btn btn-primary rounded submit px-3"
                >
                  Sign In
                </button>
                </div>
                <div class="w-50 text-md-right">
                  <a href="#">Forgot Password</a>
                </div>
              </div>
            </form>
           
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
</template>



<script>
export default {
    
}
</script>
<style>
.ftco-section{
    padding: 7em 0;
}
.justify-content-center {
    -webkit-box-pack: center!important;
    -ms-flex-pack: center!important;
    justify-content: center!important;
}
.wrap {
    width: 100%;
    overflow: hidden;
    background: #fff;
    border-radius: 5px;
    box-shadow: 0 10px 34px -15px rgb(0 0 0 / 24%);
}
@media (min-width: 768px){
    .d-md-flex {
        display: flex!important;
    }
    .p-md-5 {
        padding: 10rem 2em 0em 2em !important;
    }
}

.img, .login-wrap {
    width: 50%;
}
.img > img{
    width:100%;
}
.login-wrap {
    position: relative;
}
.d-flex {
    display: flex!important;
}
.form-group{
    text-align: left;
}
.w-100{
    width:100%;
}
.btn-primary {
    color: #fff;
    background-color: #122564;
    border-color: #18276a;
    height: 60px;
}
</style>