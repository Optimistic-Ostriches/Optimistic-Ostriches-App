<template>
  <view class="container">
    <view class="button-container">
            <button 
                title="+" 
                @press="goToAddTask"
                color="#19b1c4"
            />
    </view>
    <text class="text-time">10 : 00 am</text>
    <scroll-view :content-container-style="{contentContainer: {
        paddingVertical: 20
    }}">
        <!-- Content goes here -->
            <task-card></task-card>
            <task-card-1></task-card-1>
            <task-card-2></task-card-2>
            <task-card-3></task-card-3>
            <task-card-4></task-card-4>
    </scroll-view>
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
import TaskCard1 from "../components/TaskCard1.vue";
import TaskCard2 from "../components/TaskCard2.vue";
import TaskCard3 from "../components/TaskCard3.vue";
import TaskCard4 from "../components/TaskCard4.vue";
export default {
    props: {
        navigation: {
            type: Object
        }
    },
    components: {
        TaskCard,
        TaskCard1,
        TaskCard2,
        TaskCard3,
        TaskCard4
    },
    methods: {
        goToAddTask() {
            this.navigation.navigate("AddTask");
        }
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
.button-container {
    background-color: #072e40;
    border-radius: 80;
    width: 45;
    height: 45;
    align-items: center;
    justify-content: center;
    margin-top: 10;
    margin-left: 310;
}
.text-time {
  color: #072e40;
  padding-bottom: 16;
  font-size: 32;
  margin-top: -36;
}
.progress-bar {
    align-items: center;
    padding-top: 40;
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