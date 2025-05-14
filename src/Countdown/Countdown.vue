<template>
  <div class="countdown">
    {{ formattedCountdown }}
  </div>
</template>

<script>
export default {
  name: 'Countdown',
  props: {
    targetDate: {
      type: String,
      required: true,
    },
  },
  data() {
    return {
      currentTime: Date.now(),
      intervalId: null,
      totalHours: 0,
      minutes: 0,
      seconds: 0,
    };
  },
  computed: {
    timeLeft() {
      const targetTime = new Date(this.targetDate).getTime();
      const timeDifference = targetTime - this.currentTime;

      const seconds = Math.floor((timeDifference / 1000) % 60);
      const minutes = Math.floor((timeDifference / (1000 * 60)) % 60);
      const totalHours = Math.floor(timeDifference / (1000 * 60 * 60));

      return { totalHours, minutes, seconds };
    },
    formattedCountdown() {
      const { totalHours, minutes, seconds } = this.timeLeft;
      return `${totalHours.toString().padStart(2, '0')}:${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
    }
  },
  watch: {
    timeLeft: {
      immediate: true,
      handler(newTimeLeft) {
        this.totalHours = newTimeLeft.totalHours;
        this.minutes = newTimeLeft.minutes;
        this.seconds = newTimeLeft.seconds;
      },
    },
  },
  methods: {
    updateTime() {
      this.currentTime = Date.now();
    },
  },
  mounted() {
    this.intervalId = setInterval(this.updateTime, 1000);
  },
  beforeDestroy() {
    clearInterval(this.intervalId);
  },
};
</script>

<style scoped>
.countdown {
  padding-top: 30px;
  font-size: 60px;
  font-weight: 500;
  text-transform: none;
}
.countdown span {
  color: black;
  padding: 10px;
  border-radius: 5px;
}

@media (max-width: 450px) {
  .countdown {
    display: none;
  },
  }
</style>
