<template>
    <view class="container">
        <text class="light-text">Task Name</text>
        <text-input
            class="text-entry"
            placeholder="Name"
            v-model="taskName"
        />
        <text class="light-text">Task Notes</text>
        <text-input
            class="text-entry-long"
            placeholder="Notes"
            v-model="taskNotes"
        />
        <text class="light-text">Due Date</text>
        <text-input
            class="text-entry"
            placeholder="mm / dd / yy"
            v-model="taskDueDate"
        />
        <text class="light-text">Difficulty</text>
        <text-input
            class="text-entry"
            placeholder="1 - 5 (hard)"
            v-model="taskDifficulty"
        />
        <view class="button-container">
            <button class="button"
                title="add" 
                @press="goToDayViewScreen"
                color="#19b1c4;"
            />
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
            taskName: "",
            taskNotes: "",
            taskDueDate: "",
            taskDifficulty: ""
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
.button-container {
    background-color: #19b1c4;
    border-radius: 12;
    width: 80;
    margin-top: 14;
}
.light-text {
    color: rgb(229,255,255);
    font-size: 16;
}
.text-entry {
    background-color: #bff1f2;
    width: 240;
    height: 42;
    border-width: 1;
    border-color: #19b1c4;
    padding-left: 8;
    margin-top: 12;
    margin-bottom: 14;
    border-radius: 14;
}
.text-entry-long {
    background-color: #bff1f2;
    width: 240;
    height: 84;
    border-width: 1;
    border-color: #19b1c4;
    padding-left: 8;
    margin-top: 14;
    margin-bottom: 14;
    padding-bottom: 46;
    border-radius: 12;
}
</style>