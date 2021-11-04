<template>
  <div class="dashboard-container">
    <div class="title">{{ timeFix }}, {{ name }} !</div>
  </div>
</template>

<script>

import { timeFix } from '@/utils/utils'
import { mapState } from 'vuex'
export default {
  name: 'Dashboard',
  components: {
  },
  data() {
    return {
      timeFix: timeFix()
    }
  },
  computed: {
    ...mapState({
      name: (state) => state.user.name
    })
  }
}
</script>

<style rel="stylesheet/scss" lang="scss" scoped>
  .dashboard-container {
    color: #ccc;
    .title {
      color: #111111;
      background: #fff;
      margin: 40px;
    }
  }
</style>
