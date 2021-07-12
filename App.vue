<template>
      <view class="page" v-if="isLoading" :style="{flex: 1, backgroundColor: '#2C2F33'}">
        <status-bar background-color="#7289DA" bar-style="light-content"/>

        <!-- <text class="back-btn">Back</text> -->
        <view class="login-page" :style="{marginTop: 80}">

          <text class="header" :style="{fontSize: 28, textAlign: 'center', fontWeight: '700', marginBottom: 8}">Welcome Back!</text>
          <text class="header" :style="{fontSize: 15, color: 'gray', textAlign: 'center',  marginBottom: 50}">Login with your email and start chatting.</text>
          <view class="content-container">
              <view class="input-holder" :style="{width: '90%'}">

                <view class="input-header" :style="{widht: '100%'}">
                  <text class="input-title">Account Information</text>
                </view>
                <!-- <text :style="{color: '#fff'}">Username</text> -->
                <text-input
                  class="input"
                  :style="{borderWidth: 0, borderRadius: 5}"
                  v-model="email"
                  placeholderTextColor="rgb(141, 141, 141)"
                  placeholder="Email"
                  returnKeyType='next'
                />
                <text-input
                  class="input"
                  :style="{borderWidth: 0, borderRadius: 5}"
                  v-model="password"
                  placeholderTextColor="rgb(141, 141, 141)"
                  placeholder="Password"
                  returnKeyType='go'
                />

                <text class="pass-reset" :style="{color: '#2844aa', fontSize: 15, marginBottom: 20}">Forgot your password?</text>

                <touchable-opacity class="btn-container">
                  <text class="btn">Login</text>
                </touchable-opacity>
              </view>
          </view>
          <!-- <activity-indicator size="large" color="#0000ff" /> -->
        </view>
      </view>
</template>

<script>
export default {
  data() {
    return {
      isLoading: true,
      email: "",
      password: "",
      message: "Hello World"
    };
  },
  methods: {
    exclaim() {
      this.message += "!";
    }
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Nunito+Sans:ital,wght@0,200;0,300;0,400;0,600;0,700;0,800;0,900;1,200;1,300;1,400;1,600;1,700;1,800;1,900&display=swap');

*, body, text{
  font-family: "Nunito Sans";
}

.pass-reset{
  font-weight: 600;
}

.header{
  color: #fff;
}

.input-title{
  color: rgb(167, 163, 163);
  font-size: 13;
  font-weight: 700;
  margin-bottom: 8;
  text-transform: uppercase;
  text-align: left;
}

.content-container{
  margin: auto;
  width: 100%;
  /* background-color: red; */
  display: flex;
  align-items: center;

}

.text-color-primary {
  color: rgb(255, 94, 0);
  font-size: 30;
}

.input{
  width: 100%;
  color: rgb(255, 255, 255);
  background-color: #1e2124;
  padding: 10;
  margin-bottom: 20;
  font-size: 15.5;
  height: 50;
}

.btn-container{
  background-color: #637cd6;
  width: 100%;
  height: 50;
  border-radius: 5;
  display: flex;
  align-items: center;
  justify-content: center;
}

.btn{
  margin: auto;
  font-size: 17;
  color: #fff;
}
</style>