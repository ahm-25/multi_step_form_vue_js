<template>
  <div class="center-form">
    <keep-alive>
      <component :is="Steps[currentStep].component"></component>
    </keep-alive>
    <div class="spacing-buttons">
      <button v-if="currentStep <= Steps.length - 2" class="btn" @click="next">
        next
      </button>
      <button v-if="currentStep !== 0" class="btn" @click="prev">prev</button>
      <button v-if="currentStep === Steps.length - 1">submit</button>
    </div>
  </div>
</template>

<script>
import About from "./steps/About.vue";
import Information from "./steps/Information.vue";
import Profile from "./steps/Profile.vue";

export default {
  name: "MultiSteps",
  components: {
    About,
    Information,
    Profile,
  },
  data() {
    return {
      currentStep: 0,
      Steps: [
        {
          component: Information,
        },
        {
          component: About,
        },
        {
          component: Profile,
        },
      ],
    };
  },
  methods: {
    next() {
      this.currentStep += 1;
    },
    prev() {
      this.currentStep -= 1;
    },
  },
};
</script>

<style scoped>
.center-form {
  width: 50%;
  margin: 0 auto;
}
.btn {
  display: inline-block;
  background: #000;
  color: #fff;
  border: none;
  padding: 10px 20px;
  margin: 5px 20px;
  border-radius: 5px;
  cursor: pointer;
  text-decoration: none;
  font-size: 15px;
  font-family: inherit;
}
</style>
