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
                    <label for="" class="label">Name</label>
                    <div class="control has-icons-left">
                      <input
                        type="text"
                        class="input is-small"
                        required
                        v-model="form.name"
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
                    <button
                      @click.prevent="signup"
                      class="button is-success is-small"
                    >
                      Đăng Ký
                    </button>
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
    auth: "guest",
    data() {
      return {
        form: {
          username: "",
          name: "",
          password: "",
        },
      };
    },
    methods: {
    //   async signup() {
    //     try {
    //       await this.$store.dispatch("users/createUser", this.form);
    //       // Cập nhật thành công, thực hiện các hành động khác tại đây
    //     } catch (error) {
    //       console.error(error);
    //     }
    //   },
    },
  };
  </script>
  