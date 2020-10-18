<template>
  <view class="container">
    <image
        :style="{width:240, height: 140}"
        :source="require('../assets/logo.png')"
    />
    <view class="loginHeader">
        <text class="headerText">Let's begin!</text>
    </view>
    <view class="loginBody">
        <text-input
            class="username-input-container"
            placeholder="Username"
            v-model="username"
        />
        <text-input
            class="password-input-container"
            placeholder="Password"
            v-model="password"
        />
        <view class="button-container">
            <button 
                title="Login" 
                @press="goToDayViewScreen"
                color="#072e40"
            />
        </view>
    </view>
  </view>
</template>

<script>
export default {
    props: {
        navigation: {
            type: Object
        }
    },
    data: function() {
        return {
            username: "",
            password: ""
        };
    },
    methods: {
        goToDayViewScreen() {
            this.navigation.navigate("DayView");
        }
    }
}
</script>

<style>
.container {
  background-color:#072e40;
  align-items: center;
  justify-content: center;
  flex: 1;
}
.headerText {
  color: #072e40;
  font-size: 16;
}
.button-container {
    background-color: #19b1c4;
    border-radius: 12;
    width: 100;
}
.loginHeader {
    align-items: center;
    justify-content: center;
    width:240;
    height: 40;
    background-color: #19b1c4;
    border-top-left-radius: 12;
    border-top-right-radius: 12;
    margin-top: 20;
}
.loginBody {
    align-items: center;
    justify-content: center;
    width: 240;
    height: 260;
    background-color: #bff1f2;
    border-bottom-left-radius: 12;
    border-bottom-right-radius: 12;
}
.username-input-container {
    background-color: #bff1f2;
    width: 180;
    height: 32;
    border-width: 1;
    border-color: #19b1c4;
}
.password-input-container {
    background-color: #bff1f2;
    width: 180;
    height: 32;
    border-width: 1;
    border-color: #19b1c4;
    margin-top: 36;
    margin-bottom: 36;
}
</style>