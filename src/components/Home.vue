<template>
  <div>
    <tabs />
    <div class="flex">
      <left-side />
      <main-content />
      <right-side />
    </div>  
  </div>
</template>

<script>
import Tabs from "./Tabs.vue"
import LeftSide from "./LeftSide.vue"
import MainContent from "./MainContent.vue"
import RightSide from "./RightSide.vue"
export default {
  components: {
    Tabs,
    LeftSide,
    MainContent,
    RightSide
  }
}
</script>
