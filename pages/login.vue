<template>
    <div>
      <section class="hero is-primary is-fullheight">
        <div class="hero-body">
          <div class="container">
            <div class="columns is-centered">
              <div class="column is-5-tablet is-4-desktop is-3-widescreen">
                <form action="" class="box">
                  <div class="field">
                    <label for="" class="label">Username</label>
                    <div class="control has-icons-left">
                      <input
                        type="text"
                        class="input is-small"
                        required
                        v-model="form.username"
                      />
                      <span class="icon is-small is-left">
                        <i class="fa fa-user"></i>
                      </span>
                    </div>
                  </div>
                  <div class="field">
                    <label for="" class="label">Password</label>
                    <div class="control has-icons-left">
                      <input
                        type="password"
                        placeholder="*******"
                        class="input is-small"
                        required
                        v-model="form.password"
                      />
                      <span class="icon is-small is-left">
                        <i class="fa fa-lock"></i>
                      </span>
                    </div>
                  </div>
                  <div class="field">
                    <button @click.prevent="login" class="button is-success is-small">Login</button>
                  </div>
                </form>
              </div>
            </div>
          </div>
        </div>
      </section>
    </div>
  </template>
  
  <script>
  export default {
    layout: "none",
    auth: 'guest',
    data() {
      return {
        form: {
          username: "",
          password: "",
        },
      };
    },
    methods: {
    //   async login() {
    //     try {
    //       // console.log(this.form);
    //       await this.$auth.loginWith("local", {
    //         data: { username: this.form.username, password: this.form.password },
    //       });
    //       this.$router.push("/");
    //     } catch (error) {
    //       this.errors = error.response.data.errors;
    //     }
    //   },
    },
  };
  </script>
  