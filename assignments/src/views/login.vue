<template>
  <div>
    <div class="form">
      <form action="http://localhot:3000/signup" v-show="showLogin === false">
        <h1>הרשמה לפורום</h1>
        <div>
          <input type="text" name="name" id="name" />
          <label for="name">:שם משתמש</label>
        </div>
        <div>
          <input type="email" name="email" id="email" />
          <label for="email">:דואר אלקטרוני</label>
        </div>
        <div>
          <input type="password" name="paasword" id="password" />
          <label for="password">:סיסמה</label>
        </div>
        <button>הירשם</button>
        <div>
          <b-button type="button" @click="showlogin">sign in</b-button>
        </div>
      </form>
      <div v-show="showLogin">
        <form action="http://localhot:3000/signin">
          <h1>כניסה למשתמשים קיימים</h1>
          <div>
            <input type="email" name="email" id="email-in" />
            <label for="email">:דואר אלקטרוני</label>
          </div>
          <div>
            <input type="password" name="paasword" id="password-in" />
            <label for="password">:סיסמה</label>
          </div>
          <button>היכנס</button>
          <div>
            <b-button type="button" @click="showlogin">sign up</b-button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      showLogin: true
    };
  },
  methods: {
    showlogin() {
      if (this.showLogin) {
        this.showLogin = false;
      } else if (!this.showLogin) {
        this.showLogin = true;
      }
    }
  }
};
</script>
<style scoped>
html {
  text-align: center;
}
form {
  border: 2px solid #8299ae;
  width: 450px;
  height: 300px;
  padding: 10px;
  margin: 10px;
  display: inline-block;
}
</style>