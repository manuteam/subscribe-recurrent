<template>
  <div class="content d-flex flex-column flex-column-fluid">
    <div class="d-flex flex-column-fluid">
      <div class="container-fluid">
        <CardMain/>
        <Table
          :title="title"
        />
      </div>
    </div>
  </div>
</template>

<script>
import CardMain from "./CardMain";
export default {
  name: "HomeContent",
  components: {CardMain},
  data() {
    return {
      title: 'Subscribers'
    }
  }
}
</script>

<style scoped>

</style>
