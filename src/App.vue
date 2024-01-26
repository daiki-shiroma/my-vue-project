<template>
  <div id="app">
    <side-bar></side-bar>
    <!-- 他のコンテンツやコンポーネントがここに追加される -->
  </div>
</template>

<script>
// SideBar.vue コンポーネントをインポートします
import SideBar from './components/SideBar.vue';

export default {
  name: 'App',
  components: {
    // SideBar コンポーネントを登録します
    'side-bar': SideBar
  }
  // App コンポーネントのデータやメソッドもここに追加できます。
};
</script>

<style>
/* ここにグローバルなスタイルを追加できます */
</style>
