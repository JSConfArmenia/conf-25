<template>
  <div class="TimeScale">
    <div
      v-for="(block, index) in timeBlocks"
      :key="index"
      class="Item"
      :style="{
        flexBasis: `${block.duration * 3}px`,
        height: `${block.duration * 3}px`,
      }">
      <div class="Label">
        {{ getTime(block.start) }}
      </div>
      <div class="Ruller"></div>
    </div>
  </div>
</template>

<script>
import moment from 'moment';

export default {
  props: ['start', 'topics'],
  data: () => ({
    timeScale: Array.from(Array(40)).map((item, index) => (index * 15)),
  }),
  computed: {
    minuteHeight() {
      return 3;
    },
    timeBlocks() {
      if (!this.topics || !this.topics.length) {
        return Array.from(Array(40)).map((item, index) => ({ index, duration: 15 }));
      }

      let startCounter = 0;

      return this.topics.map((topic, index) => {
        const block = {
          index,
          duration: topic.duration,
          start: startCounter,
          end: startCounter + topic.duration,
        };

        startCounter += block.duration;

        return block;
      });
    },
  },
  methods: {
    getTime: function getTime(minutesPassed = 0) {
      return moment(new Date(`10/23/2021 ${this.start}:00`)).add(minutesPassed, 'm').format('H:mm');
    },
  },
  mounted: function mounted() {

  },
};
</script>

<style scoped>

  .TimeScale {
    position: absolute;
    left: 0;
    right: 0;
  }

  .Item {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    /* height: 45px; */
    /* flex-basis: 45px; */
  }

  .Label {
    flex: 0;
    padding-right: 10px;
    padding-left: 10px;
    text-align: right;
    font-size: .9em;
    position: relative;
    top: -11px;
  }

  .Ruller {
    flex: 1;
    height: 1px;
    background-color: rgba(0, 0, 0, 0.2);
  }

  .Item:nth-child(odd) .Ruller {
    /* background-color: #e23f72; */
  }

  .Item:nth-child(even) .Ruller {
    margin-left: 5px;
  }

  @media (max-width: 768px) {
    .TimeScale {
      font-size: .9em;
    }

    .Label {
      /* padding-left: 0; */
      padding-left: 15px;
      padding-right: 5px;
    }
  }
</style>
