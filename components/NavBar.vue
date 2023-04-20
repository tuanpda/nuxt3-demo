<template>
    <div>
      <nav class="navbar is-light" role="navigation" aria-label="main navigation">
        <div class="navbar-brand">
          <a class="navbar-item" href="https://bulma.io">
            <img
              src="https://bulma.io/images/bulma-logo.png"
              width="112"
              height="28"
            />
          </a>
  
          <a
            role="button"
            class="navbar-burger"
            aria-label="menu"
            aria-expanded="false"
            data-target="navbarBasicExample"
          >
            <span aria-hidden="true"></span>
            <span aria-hidden="true"></span>
            <span aria-hidden="true"></span>
          </a>
        </div>
  
        <div id="navbarBasicExample" class="navbar-menu">
          <div class="navbar-start">
            <a class="navbar-item"> Home </a>
  
            <a class="navbar-item"> Documentation </a>
  
            <div class="navbar-item has-dropdown is-hoverable">
              <a class="navbar-link"> Admin </a>
  
              <div class="navbar-dropdown">
                <a class="navbar-item" href="/admin/users/"> Users </a>
                <a class="navbar-item"> Jobs </a>
                <a class="navbar-item"> Contact </a>
                <hr class="navbar-divider" />
                <a class="navbar-item"> Report an issue </a>
              </div>
            </div>
          </div>
  
          <div class="navbar-end">
            <div class="navbar-item has-dropdown is-hoverable">
              <template v-if="userinfo != null">
                <a class="navbar-link">
                  <img alt="" width="40" height="40" style="border-radius: 50%" />
                  &ensp; 
                </a>
  
                <div
                  ref="navbarDropDown-6"
                  class="navbar-dropdown is-boxed"
                  @click="closeNavbar(6)"
                >
                  <a class="navbar-item"> About </a>
                  <a class="navbar-item"> Jobs </a>
                  <a class="navbar-item"> Contact </a>
                  <hr class="navbar-divider" />
                  <a class="navbar-item"> Đăng xuất </a>
                </div>
              </template>
            </div>
          </div>
        </div>
      </nav>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        userinfo: null,
      };
    },
  
    // created() {
    //   // console.log(this.$auth.$state.user);
    //   const user = this.$auth.$state.user;
    //   if (user !== null) {
    //     this.userinfo = user;
    //   }
    // },
  
    methods: {
      closeNavbar(num) {
        this.$refs[`navbarDropDown-${num}`].style.display = "none";
        setTimeout(() => {
          this.$refs[`navbarDropDown-${num}`].style.display = "block";
        }, 300);
      },
  
    },
  };
  </script>
  