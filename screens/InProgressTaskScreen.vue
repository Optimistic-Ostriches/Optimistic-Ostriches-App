<template>
  <view class="container">
    <text class="working-text">You are working on...</text>
    <view class="current-task">
        <text class="task-name">Science Project</text>
        <text class="task-notes">Notes</text>
    </view>
  </view>
</template>

<style>
.container {
    background-color: #19b1c4;
    align-items: center;
    justify-content: center;
    flex: 1;
}
.working-text {
  color:  #072e40;
}
.current-task {
    background-color:  #072e40;
    align-items: center;
    justify-content: center;
}
.current-task-name {
    font-size: 24;
    color: #bff1f2;
    justify-content: center;
}
.current-task-notes {
    padding-top: 24;
    padding-left: 36;
    padding-right: 36;
    padding-bottom: 24;
    font-size: 12;
    color: #bff1f2;
}
</style>