<template>
  <div id="home">
    <div class="main">
      <div class="main-blue">
        <div class="main-blue__todo">
          <img src="../assets/logo.png" alt="logo" />
          <div class="main-blue__todo-box">
            <div class="list container">
              <div class="list-1 box-lis">
                <input v-show="list" v-model="list1" />
                <h2 v-show="!list">1.{{list1}}</h2>
                <button @click="list = !list">
                  <img src="../assets/pencil.png" alt="pencil" />
                </button>
              </div>
              <div class="list-1 box-lis">
                <input v-show="list2" v-model="list12" />
                <h2 v-show="!list2">2.{{list12}}</h2>
                <button @click="list2 = !list2">
                  <img src="../assets/pencil.png" alt="pencil" />
                </button>
              </div>
              <div class="list-3 box-lis">
                <input v-show="list3" v-model="list13" />
                <h2 v-show="!list3">3.{{list13}}</h2>
                <button @click="list3 = !list3">
                  <img src="../assets/pencil.png" alt="pencil" />
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
export default {
  name: 'HomeView',
  props: {
    msg: String,
  },
  data: () => ({
    list1: 'Morning call with team',
    list12: 'Healhy breakfast',
    list13: 'Morning training at the gym',
    list: false,
    list2: false,
    list3: false,
  }),
  // methods: {
  //   changeText() {
  //     this.list1 = '';
  //   },
  // },
};
</script>
<style scoped lang="scss">
.box-lis {
  display: inline-flex;
  button {
    background: none;
    border: none;
    font-size: 14px;
    display: inline-flex;
    align-items: center;
    img {
      width: 50px;
    }
  }
}
.list {
  display: flex;
  flex-direction: column;
  margin-top: 10px;
  justify-content: center;
  height: 100%;
  align-items: center;
  h2 {
    color: grey;
  }
  input {
    font-size: 25px;
  }
}
#home {
  height: 100%;
  background-color: #e5e5e5;
}
.main {
  height: 100%;
  width: 100%;
  &-blue {
    height: 70%;
    background: linear-gradient(
      0deg,
      rgba(0, 86, 154, 1) 0%,
      rgba(0, 175, 237, 1) 100%
    );
    &__todo {
      display: inline-flex;
      flex-direction: column;
      width: 100%;
      height: 100%;
      margin-top: 4%;
      align-items: center;
      img {
        width: 10%;
      }
      &-box {
        height: 45%;
        width: 56%;
        background: white;
        position: absolute;
        left: 22%;
        top: 32%;
      }
    }
  }
}
</style>
