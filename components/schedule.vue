<template>
  <div class="schedule">
    <div class="size margin content" id="schedule">
      <div class="container justify-content-center">
        <div class="box-title text-align-center">
          <h2>Programação</h2>
        </div>
      </div>
      <div class="schedule-container container column">
        <div
          class="schedule--item container align-items-start"
          v-for="schedule in schedules"
          :key="schedule.id"
          :class="{ active : sheduleSelected === schedule.id}"
          v-on:mouseover="sheduleSelected = schedule.id"
        >
          <div class="schedule--item--time margin-right-10">
            <strong class="margin-bottom-20">{{schedule.time}}</strong>
          </div>

          <div class="schedule--item--ball container justify-content-center">
            <div class="line"></div>
            <div class="ball"></div>
          </div>

          <div class="schedule--item--description">
            <h4 class="title">{{schedule.title}}</h4>
            <strong class="subtitle" v-if="schedule.name">{{schedule.name}}</strong>
            <p v-if="schedule.description">{{schedule.description}}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { mapState } from "vuex";

export default {
  data() {
    return {
      sheduleSelected: 1
    };
  },
  computed: {
    ...mapState(["schedules"])
  }
};
</script>

<style lang="scss" scoped>
@import "~assets/sass/components/schedule.scss";
</style>
