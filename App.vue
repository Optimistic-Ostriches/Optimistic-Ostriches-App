<template>
  <app-navigator></app-navigator>
</template>

<script>
import {
  createAppContainer,
  createStackNavigator
} from "vue-native-router";

import LoginScreen from "./screens/LoginScreen.vue";
import DayViewScreen from "./screens/DayViewScreen.vue";
import InProgressTaskScreen from "./screens/InProgressTaskScreen.vue";
import AddTaskScreen from "./screens/AddTaskScreen.vue";

const StackNavigator = createStackNavigator(
  {
    Login: LoginScreen,
    DayView: DayViewScreen,
    InProgressTask: InProgressTaskScreen,
    AddTask: AddTaskScreen
  },
  {
    initialRouteName: 'Login'
  }
);

const AppNavigator = createAppContainer(StackNavigator);
export default {
  components: { AppNavigator }
}
</script>