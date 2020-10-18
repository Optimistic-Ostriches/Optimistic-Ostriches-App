<template>
    <view>
        <view class="card">
            <text class="taskName">Science Project</text>
            <text class="taskNotes">These are the notes you entered when you added this task. The notes will help you remember specific things related to the task.</text>
            <text class="recText">Recommended now!</text>
            <button
                title="Let's do it!"
                color="#072e40"
            />
            <text class="taskTime">1 hour</text>
        </view>
    </view>
</template>

<style>
.card {
  background-color: #19b1c4;
  align-items: center;
  justify-content: center;
  height: 350;
  width: 240;
  margin-bottom: 20;
  border-radius: 12;
  /*flex: 1;*/
}
.taskName {
    font-size: 24;
    color: #072e40;
    justify-content: center;
}
.taskNotes {
    padding-top: 32;
    padding-left: 36;
    padding-right: 36;
    padding-bottom: 32;
    font-size: 12;
    color: #072e40;
}
.recText {
    padding-bottom: 10;
}
.taskTime {
    padding-top: 32;
    color: #bff1f2;
    font-size: 20;
}
</style>
