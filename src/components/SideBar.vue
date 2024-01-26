<template>
  <div class="sidebar">
    <div class="sidebar-item" v-for="(item, index) in steps" :key="index" @click="selectStep(index)">
      <div class="status-icon" :class="{ 'complete': index < selectedStep, 'current': index === selectedStep }"></div>
      <span>{{ item }}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SideBar',
  data() {
    return {
      selectedStep: 0, // 最初のステップが選択されている状態
      steps: [
        'Enter company information',
        'Describe position details',
        'Define skills/competences',
        'Set Interview objectives and goals',
        'Select an interview to join',
        'Finalize setup'
      ]
    };
  },
  methods: {
    selectStep(index) {
      this.selectedStep = index;
    }
  }
};
</script>

<style scoped>
.sidebar-item {
  cursor: pointer;
  /* 他のスタイル */
}

.status-icon {
  /* 共通のスタイル */
}

.status-icon.complete {
  background-color: green;
  /* 完了したステップのスタイル */
}

.status-icon.current {
  background-color: blue;
  /* 現在選択中のステップのスタイル */
}
</style>
