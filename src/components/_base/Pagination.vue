<template>
    <div class="container-page">
<nav aria-label="...">
  <ul class="pagination">
    <li class="page-item disabled">
      <a class="page-link" href="#">Prev</a>
    </li>
    <li class="page-item" :class="n==data.curentPage? 'active':''" v-for="n in data.totalPage" :key="n"><a class="page-link" href="#" @click.prevent="$emit('send-event', n)">{{n}}</a></li>
    <!-- <li class="page-item active" aria-current="page">
      <a class="page-link" href="#">2 <span class="sr-only">(current)</span></a>
    </li>
    <li class="page-item"><a class="page-link" href="#">3</a></li> -->
    <li class="page-item">
      <a class="page-link" href="#">Next</a>
    </li>
  </ul>
</nav>
    </div>
</template>

<script>
export default {
  name: 'Pagination',
  props: {
    data: {
      type: Object
    }
  }
}
</script>

<style scoped>

</style>
