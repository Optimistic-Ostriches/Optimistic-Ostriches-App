<template>
    <view>
        <view class="card">
            <text class="task-name">Reading Homework</text>
            <text class="task-notes">Here are some more notes. Maybe you entered a link to the online book.</text>
            <!-- <text class="rect-text">Recommended now!</text> -->
            <view class="button-container">
                <button
                    title="Let's do it!"
                    color="#19b1c4"
                />
            </view>
            <text class="task-time">30 mins</text>
        </view>
    </view>
</template>

<style>
.card {
  background-color: #19b1c4;
  align-items: center;
  justify-content: center;
  /*height: 350;
  width: 240;*/
  height: 380;
  width: 260;
  margin-bottom: 16;
  border-radius: 12;
}
.task-name {
    font-size: 24;
    color: #072e40;
    justify-content: center;
}
.task-notes {
    padding-top: 24;
    padding-left: 36;
    padding-right: 36;
    padding-bottom: 24;
    font-size: 12;
    color: #072e40;
}
.rect-text {
    padding-bottom: 10;
    font-size:12;
    color: #bff1f2;
}
.button-container {
    background-color: #072e40;
    border-radius: 12;
    width: 160;
    height: 50;
}
.task-time {
    padding-top: 16;
    color: #bff1f2;
    font-size: 20;
}
</style>
