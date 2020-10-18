<template>
  <view class="container">
    <text class="text-time">10 : 00 am</text>
    <task-card></task-card>
    <view class="progress-bar">
            <text class="prog-text">Today's Progress</text>
            <view class="bar">
                <view class="progress"></view>
            </view>
     </view>
  </view>
</template>

<script>
import TaskCard from "../components/TaskCard.vue";
export default {
    props: {
        navigation: {
            type: Object
        }
    },
    components: {
        TaskCard
    }
}
</script>

<style>
.container {
  background-color: rgb(229,255,255);
  align-items: center;
  justify-content: center;
  flex: 1;
}
.text-time {
  color: #072e40;
  padding-bottom: 16;
  font-size: 32;
}
.progress-bar {
    align-items: center;
    padding-top: 10;
}
.prog-text {
    color: #072e40;
}
.bar {
    background-color: #072e40;
    height: 24;
    width: 240;
    border-radius: 12;
    margin-top: 10;
}
.progress {
    background-color: #19b1c4;
    height: 16;
    width: 40;
    margin-top: 4;
    margin-left: 4;
    border-radius: 12;
}
</style>