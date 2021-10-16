<template>
  <div>
    <h1>기술스택</h1>
    <v-divider />
    <Treeview />
  </div>
</template>

<script>
// @ is an alias to /src
import Treeview from "@/components/common/Treeview.vue";  

export default {

  name: "Home",
  components: {
    Treeview,
  },
  }

</script>
