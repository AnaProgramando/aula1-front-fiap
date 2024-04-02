<template id="app">
  <img src="../../img/logo.png" width="40px" height="40px" />
  <h1 class="titulo">Sign in to GitHub</h1>
  <form name="login-form" action="/login" method="post">
    <label class="username-password">
      Username or email address
      <input type="text" name="username" />
    </label>
    <div class="password-wrapper">
      <label class="username-password" for="password">
        <span>
          Password
          <a href="#" class="forgot-password">Forgot password?</a>
        </span>
        <input id="password" name="password" />
      </label>
    </div>
    <button class="button-signin">Sign in</button>
  </form>
  <div class="box-forgot-password">
    <a href="#" class="button-signin-key">Sign in with a passkey</a>
    <div>
      New to GitHub?
      <a href="#" class="button-signin-key">Create an account</a>
    </div>
  </div>
</template>

<style scoped>
#app {
  display: flex;
}

.titulo {
  font-size: 24px;
  font-weight: var(--base-text-weight-light, 300);
  letter-spacing: -0.5px;
}

.username-password {
  display: block;
  margin-bottom: 8px;
  font-weight: var(--base-text-weight-normal, 400);
  text-align: left;
}

form {
  background: #eee;
  border-radius: 4px;
  padding: 20px;
  width: 288px;
  margin: 0 auto;
}

.box-forgot-password {
  background: #fff;
  border-radius: 4px;
  padding: 20px;
  width: 288px;
  margin: 0 auto;
}

.input {
  padding: 4px;
  width: 100%;
}

.button-signin {
  background-color: green;
  color: #fff;
  display: block;
  width: 100%;
  text-align: center;
}

.button-signin-key {
  grid-area: text;
  line-height: var(--text-body-lineHeight-medium, 1.4285);
  white-space: nowrap;
  color: blue;
  font-weight: var(--base-text-weight-light, 300);
}

.password-wrapper {
  margin-bottom: 24px;
  position: relative;
}

.forgot-password {
  float: right;
  font-size: 12px;
}
</style>
