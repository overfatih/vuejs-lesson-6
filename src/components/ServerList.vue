<template>
    <div class="row">
        <Servers/>          
        <ServerStatus/>
    </div>
</template>

<script>
import Servers from './Servers';
import ServerStatus from './ServerStatus'

export default {
  components:{
      Servers,
      ServerStatus
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
