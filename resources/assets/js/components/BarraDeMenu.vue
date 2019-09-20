<template>
  <nav v-bind:class="'navbar navbar-expand-lg bg-' + cor">
  <a class="navbar-brand" href="#">{{titulo}}</a>
</nav>
</template>

<script>
export default {
    props:['titulo', 'cor']
}
</script>

<style type="text/css">
    .navbar-brand {
        color: white;
        font-weight: bold;
    }
</style>