<template>
  <div>
    <b-container class="container-main" fluid style="padding-left: 0; padding-right: 0">
      <b-row>
        <b-col cols="2" class="col">
          <input
            type="search"
            id="form1"
            class="form-control"
            placeholder="Search"
            aria-label="Search"
          />
          <hr />
          <b-nav vertical class="w-25, nav-bar">
            <b-nav-item>Home</b-nav-item>
            <b-nav-item>Orders</b-nav-item>
            <b-nav-item>Profile</b-nav-item>
            <b-nav-item>Contact</b-nav-item>
            <b-nav-item>Address</b-nav-item>
          </b-nav>
        </b-col>
        <b-col cols="10" class="div-table">
           <b-container fluid style="border-right: 1px solid black">
            <b-row sm="12">
                <b-col cols="12" class="header" style="display:inline-flex"> order Status
                    <div style="right: 20px;position: absolute;">
                    <b-dropdown size="lg" ropleft text="Drop-Left" variant="link" toggle-class="text-decoration-none" no-caret>
                        <template #button-content>
                        &#x1f50d;<span class="sr-only">Search</span>
                        </template>
                        <b-dropdown-item href="#">Action</b-dropdown-item>
                        <b-dropdown-item @click="logout()">Logout</b-dropdown-item>
                    </b-dropdown>
                    </div>    
                </b-col>
            </b-row>
            </b-container>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
export default {
    data(){

    },
    methods:{
        getCookie(name) {
            var nameEQ = name + "=";
            var ca = document.cookie.split(";");
            for (var i = 0; i < ca.length; i++) {
                var c = ca[i];
                while (c.charAt(0) == " ") c = c.substring(1, c.length);
                if (c.indexOf(nameEQ) == 0) return c.substring(nameEQ.length, c.length);
            }
            return null;
        },
        eraseCookie(name) {   
            document.cookie = name +'=; Path=/; Expires=Thu, 01 Jan 1970 00:00:01 GMT;';
        },
        logout(){
            this.eraseCookie("username");
            this.$router.push("/");
        }
    },
    created(){
        if(!this.getCookie('username')){
            this.$router.push("/");
        }
    }
}
</script>

<style>
.nav-bar {
  font-family: emoji;
  padding: 12px;
  font-size: 23px;
}
.col {
  height: 100vh;
  color: #fff;
    background-color: #122564;
  box-shadow: 5px 5px 11px 0px #ccc;
}
.col ul li a {
  color: #fff;
}
.form-control {
  margin-top: 13px;
}
.header {
  box-sizing: border-box;
  background-color: #c1e0de;
  height: 30%;
  font-size: 35px;
  font-family: fantasy;
  color: #3781b1;
  box-shadow: 5px 10px 8px #888888;
}
.container-main{
    width:98%
}
</style>