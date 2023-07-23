<template>
  <div class="post-list">

    <div v-for="post in posts" :key="post.id">
      <SinglePost :post="post"/>
    </div>

  </div>
</template>
<script>
import SinglePost from "@/components/Singlepost";
import {onMounted,onUnmounted,onUpdated} from "vue";

export default {
  components: {SinglePost},

  props: ['posts'],
  setup: function (props) {
    onMounted(() => console.log('comp mounted'))
    onUnmounted(() => console.log('comp unmounted'))
    onUpdated(() => console.log('comp updated'))
  }
}

</script>


<style>


</style>