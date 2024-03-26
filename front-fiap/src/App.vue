<script setup>
import HelloWorld from './components/HelloWorld.vue'
</script>

<template id="app">
      <img src="../../img/logo.png" width="40px" height="40px" />
      <h1 class="titulo">Sign in to GitHub</h1>
      <form name="login-form" action="/login" method="post">
        <label
          >Username or email address
          <input type="text" name="username" />
        </label>
        <div class="password-wrapper">
          <label for="password"
            >Password            
            <input id="password" name="password" />
            <a href="#" class="forgot-password">Forgot password?</a>
          </label>
        </div>
        <button>Sign in</button>
      </form>
      <div>
        <a href="#" class="forgot-password"
          ><strong>Sign in with a passkey</strong></a
        >
        <div>
          New to GitHub?
          <a href="#" class="forgot-password">Create an account</a>
        </div>
      </div>
</template>

<style scoped>
  .titulo {
    color: blue;
    font-size: 50px;
    background: #cde;
  }

  #app {
    display: flex;
  }

  form {
    background: #eee;
    border-radius: 4px;
    padding: 20px;
    width: 288px;
    margin: 0 auto;
  }

  .input {
    padding: 4px;
    width: 100%;
  }

  .password-wrapper {
    margin-bottom: 24px;
    position: relative;
  }

  .forgot-password {
    position: absolute;
    right: 0;
    top: 0;
  }

  button {
    padding: 8px 12px;
  }
</style>
