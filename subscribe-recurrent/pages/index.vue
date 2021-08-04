<template>
  <div class="d-flex flex-column flex-row-fluid wrapper">
    <Header/>
    <HomeContent/>
    <Footer/>
  </div>
</template>

<script>
import HomeContent from "../components/HomeContent";
export default {
  components: {HomeContent}
}
</script>
