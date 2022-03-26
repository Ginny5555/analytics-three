<template>
  <div id="about">
    <div class="main">
      <div class="main-grey"></div>
      <div class="main-gradient">
        <div class="container main-gradient__img">
          <img src="../assets/logo.png" alt="logo" />
        </div>
      </div>
      <div class="main-pic">
        <img src="../assets/bacg-laptop.png" alt="laptop" />
        <div class="main-pic-head">
          <div class="container">
            <h1>
              Welcome to
              <br />Business Analytics Online
            </h1>
          </div>
        </div>
      </div>

        <div class="main-list">
          <div class="container">
          <div class="main-list__box">

           <p> <b>Business Analytics</b> -
            convenient tool for managing and forecasting your business
            performance, which will help analyze your own finances and cash flows,
            visualize your reporting, business processes, KPI's
— a new</p>
            <ul>
              <li>
                <h3>Interactive Reporting</h3>In just a few clicks,
                you can connect your data from 1C, CRM
                (Bitrix24, AmoCRM, ZohoCRM), E-commerce
                (PROM.UA, Rozetka, ebay), Logistic (Nova Poshta),
                Google Analytics and many more systems that reflect
                different aspects of business activities.
              </li>
              <li>
                <h3>Automated data updates</h3>The application automatically
                updates and structures the data in just 60 seconds, saving you time and money.
              </li>
              <li>
                <h3>Data Security</h3>The Bank guarantees the safety
                of your personal data, ensuring their integrity and confidentiality.
              </li>
            </ul>
          <!-- <div class="main-list__form">
            <div class="main-list__form-box">
              <input v-model="message" placeholder="отредактируй меня" />
              <input />
              <button>login</button>
              <a href>Forgot password</a>
              <span>
                <a href>Register now</a>
              </span>
            </div>
          </div> -->
</div>
        </div>
      </div>
      <div class="main-footer">
        <div class="container">
          <div class="main-footer__links">
            <img src="../assets/logo.png" alt="logo" />
            <div class="main-footer__links-privacy">
              <a href="/">Terms & Conditions</a>
              <a href="/">Privacy</a>
              <a href="/">Notice at Collection</a>
              <a href="/">CA Privacy Hub</a>
              <a href="/">Contact Us</a>
              <a href="/main">Sitemap</a>
            </div>
          </div>
          <hr />
          <div class="main-footer__copyright">
            <h5>
              Copyright © 2020 Citigroup Inc. Citibank,
              N.A. Member FDIC. Equal Opportunity Lender.
            </h5>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
// @ is an alias to /src
export default {
  name: 'AboutView',
  props: {
    msg: String,
  },
};
</script>
<style scoped lang="scss">
@mixin greyCol {
  background-color: #333333;
}
@mixin rowInline {
  display: inline-flex;
  flex-direction: row;
  justify-content: space-between;
}
#about {
  height: 100%;
}
.main {
  height: 100%;
  background-color: #e5e5e5;
  &-grey {
    @include greyCol;
    height: 4%;
  }
  &-gradient {
    height: 9%;
    background: linear-gradient(
      0deg,
      rgba(0, 86, 154, 1) 0%,
      rgba(0, 175, 237, 1) 100%
    );
    &__img {
      height: 100%;
      display: flex;
      align-items: center;
      img {
        height: 70%;
      }
    }
  }
  &-pic {
    height: 33%;
    display: flex;
    flex-grow: 100;
    position: relative;
    width: 100%;
    img {
      height: 100%;
      display: flex;
      flex-grow: 100;
      width: 100%;
    }
    &-head {
      position: absolute;
      width: 100%;
      height: 100%;
      display: flex;
      align-items: end;
      h1 {
        color: white;
        width: 60%;
      }
    }
  }
  &-footer {
    @include greyCol;
    height: 16%;
    bottom: 0;
    // position: absolute;
    width: 100%;
    &__links {
      @include rowInline;
      width: 100%;
      img {
        height: 35px;
      }
      &-privacy {
        @include rowInline;
        width: 62%;
        align-items: center;
      }
    }
  }
  &-list {
    // height: 38%;
    background-color: #e5e5e5;
    display: flex;
    flex-direction: row;

    &__form {
      &-box {
        padding: 30px 30px 0;
        position: absolute;
        background: #ffffff;
        width: 20%;
        height: 30%;

        top: 29%;
        display: inline-flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: center;
        label {
          text-align: left;
        }
        input {
          width: 93%;
          height: 11%;
        }
        button {
          width: 93%;
          height: 11%;
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
    &__box {
      width: 66%;
           margin-top: 20px;

      ul {
        li::before {
          content: "";
          background: url("../assets/vector.png") no-repeat;
          width: 23px;
          height: 17px;
          position: absolute;
          left: 11%;
        }
      }
    }
  }
}

</style>
<style lang="scss">
html{
   height: 100%;
}
body {
  margin: 0;
  font-family: Roboto;
height: 100%;
}
.container {
  width: 70%;
  margin: 0 auto;
  height: auto;
  overflow: hidden;
}
h1 {
  font-weight: 400;
  font-style: Regular;
  font-size: 55px;
  line-height: 86.18px;
}
p {
  font-size: 16px;
  line-height: 22px;
}
ul li {
  font-size: 14px;
  line-height: 22px;
  list-style-type: none;
  font-weight: 400!important;
}
a {
  color: white;
  text-decoration: none;
}
h5 {
  color: white;
}
h3 {
  font-weight: 500!important;
  font-size: 16px;
  margin:10px 0;
}
</style>
