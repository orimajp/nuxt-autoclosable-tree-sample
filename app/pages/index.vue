<template>
  <div class="container">
    <div class="side-bar">
      <TreeSidebar @selectId="selectId" />
    </div>
    <div class="main-content">
      <Page :selected-id="selectedId" />
    </div>
  </div>
</template>

<script>
import TreeSidebar from '../components/TreeSidebar'
import Page from '../components/Page'

export default {
  components: {
    TreeSidebar,
    Page
  },
  data: () => ({
    selectedId: 'unselected'
  }),
  methods: {
    selectId(id) {
      this.selectedId = id
    }
  }
}
</script>

<style scoped>
.container {
  text-align: center;
  margin: 100px;
}
.side-bar {
  float: left;
  text-align: left;
  width: 40%;
}
.main-content {
  float: left;
  text-align: left;
  width: 60%;
}
</style>
