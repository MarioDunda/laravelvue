<template>
  <div class="container">
      <div v-if="this.loading">
          <feed-principal v-bind:lista="this.lista"></feed-principal>
      </div>
  </div>
</template>

<script>
export default {
    data(){
        return{
            loading: false,
            lista:[]
        }
    },
    mounted: function() {
        axios.get('/api/noticias').then(response => {
            this.lista = response.data;
            this.loading = true;
        })
    }
}
</script>

<style type="text/css">
    .navbar-brand {
        color: white;
        font-weight: bold;
    }
</style>