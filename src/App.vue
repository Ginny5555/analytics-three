<template>
  <div id="app">
    <AboutView v-show="showText" />
    <div class="container">
      <div class="main-list__form" v-show="showText">
        <div class="main-list__form-box">
          <label for="username">
            Name
            <input id="username" v-show="validate" v-model="message" />
            <small v-show="validate"></small>
            <input id="username" v-if="message === login" v-show="!validate" v-model="message" />

            <input id="username" v-else v-show="!validate" class="border" v-model="message" />
            <small v-show="!validate">Enter your name</small>
          </label>

          <label for="password">
            Password
            <input id="password" v-show="validate" v-model="passw" />
            <small v-show="validate"></small>
            <input id="password" v-if="passw === password" v-show="!validate" v-model="passw" />

            <input id="password" v-else v-show="!validate" class="border" v-model="passw" />
            <small v-show="!validate">Enter your number</small>
          </label>

          <button
            v-on:click="showText = !showText"
            v-if="message === login && passw === password "
          >login</button>
          <button class="btn" v-on:click="validate = !validate" v-else>login</button>
          <a href>Forgot password</a>
          <span>
            <a href>Register now</a>
          </span>
        </div>
      </div>
    </div>
    <HomeView v-show="!showText" />
    <h1 class="thank" v-show="!showText">Thank you,{{message}}!</h1>
  </div>
</template>
<script>
import AboutView from '@/views/AboutView.vue';
import HomeView from '@/views/HomeView.vue';

export default {
  name: 'App',
  components: {
    AboutView,
    HomeView,
  },
  data: () => ({
    passw: '',
    message: '',
    login: 'Admin',
    password: '12345',
    showText: true,
    validate: true,
  }),
};
</script>
<style lang="scss" >
.thank {
  font-size: 42px;
  top: 33%;
  position: absolute !important;
  text-align: center;
  width: 100%;
}

small {
  color: red;
}

label {
  width: 100%;
}
.border {
  border-color: red;
}

#app {
  height: 100%;
}
.val {
  width: 100%;
}
.main-list__form {
  display: flex;
  justify-content: flex-end;
  &-box {
    padding: 30px 30px 0;
    position: absolute;
    background: #ffffff;
    width: 20%;
    height: 32%;
    box-shadow: 2px 2px 15px #000000 10%;
    top: 33%;
    display: inline-flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    label {
      text-align: left;
      color: #333333;
      font-weight: 100;
      font-size: 18px;
      line-height: 21px;
    }
    input {
      width: 98%;
      height: 50px;
      font-size: 25px;

      &:focus {
        border: 1px solid #101010;
      }
    }

    button {
      width: 100%;
      height: 50px;
      font-size: 22px;
      background: #0076c0;
      text-transform: uppercase;
      border: none;
      color: #ffffff;
      &:hover {
        background: #ffffff;
        color: #0076c0;
        border: 2px solid #0076c0;
      }
    }
    a {
      color: #056dae;
      font-size: 20px;
    }
    span {
      background: #f6f6f6;
      width: 100%;
      height: 11%;
      padding: 15px 30px;
      text-align: center;
      a {
        color: #333333;

        font-size: 25px;
        line-height: 29px;
      }
    }
  }
}

@media (max-width: 420px){
 .main-pic-head {
   h1{
    font-size: 25px!important;}
 }

}
@media (min-width: 900px){
 .main-list{
        height: 38%!important;
  }
   .main-list__form-box {
    height:40%;
    top:28%;
  }
}
@media (max-width: 800px) {
  h5{
    margin:0;
  }
  .container {
    width: 90%;
  }
  .main-footer__links-privacy {
    display: none !important;
  }
  .main-list__form-box {
    width: 32%;
    height: 30%;
    left: 49%;
    top: 13%;
  }
  .main-list__box {
    width: 90% !important;
  }
  .main-pic-head h1 {
    width: 50%!important;
    line-height: 50px !important;
    font-size: 32px !important;
  }
  a {
    font-size: 10px !important;
  }
  .main-pic-head h1 {
    line-height: 83px;
  }
}
@media (max-width: 1100px) {
  .thank {
    font-size: 35px;
  }
  .main-footer__links-privacy {
    width: 80% !important;
    font-size: 10px;
  }
  .main-list__form-box {
    width: 32%;
    height: 30%;
    left: 49%;
    top: 13%;
  }
  .main-list__box {
    width: 90% !important;
  }
  .main-blue__todo-box {
    height: 60% !important;
  }

  a {
    font-size: 12px !important;
  }
  .main-pic-head h1 {
    line-height: 83px;
  }
  .main-list__box {
    margin-top: 20px !important;
  }
  h3 {
    margin: 10px 0;
    font-size:14px;
  }
}
@media (max-width: 1500px) {
  .main-list__form-box label{
    font-size:14px;

  }
  .thank {
    top: 27%;
  }
  .container {
    width: 80%;
  }
  .main-footer__links-privacy {
    width: 80%;
    font-size: 12px;
  }
  a {
    font-size: 12px !important;
  }
  input {
    height: 30px !important;
  }
  button {
    height: 32px!important;
  }
  h1 {
    font-size: 42px;
  }
  h3{
    font-size: 12px;
    margin: 5px 0;
  }
  p,ul li{
    font-size: 10px;
  }

}

@media (min-width: 1750px) {
  .container {
    width: 60%;
  }
  .main-list{
        height: 38%!important;
  }
  .main-list__box {
    ul {
      li::before {
        left: 20% !important;
      }
    }
  }
}
</style>
