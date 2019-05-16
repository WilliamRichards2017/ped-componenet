<template>
  <div id="app">
    <Pedigree pedTxtProp="1408 1011 1012 1014 2 0\n
    1408 1012 1020 1019 1 0 \n
    1408 1013 1012 1014 1 0 \n
    1408 1014 1018 1017 2 0 \n
    1408 1015 1012 1014 1 0 \n
    1408 1016 1012 1014 1 0 \n
    1408 1017 0 0 2 0 \n
    1408 1018 0 0 1 0 \n
    1408 1019 0 0 2 0 \n
    1408 1020 0 0 1 0 \n">

    </Pedigree>


  </div>
</template>

<script>
import Pedigree from './components/Pedigree.vue'

export default {
  name: 'app',
  components: {
    Pedigree
  }
}
</script>

<style>
#app {

}
</style>
