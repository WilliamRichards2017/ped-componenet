<template>
  <div class="Pedigree">
    <h1>{{ pedTxtProp }}</h1>
  </div>
</template>

<script>

  import * as pedigreejs from '../js/pedigreejs';
  import 'd3';



  export default {
  name: 'Pedigree',
  props: {
    pedTxtProp: String
  },
  data() {
    return{
      pedTxt : this.pedTxtProp,
      opts: {
        "targetDiv": "pedigree",
        labels: ['alleles', 'NA']
      }
    }
  },
  beforeMount(){
    this.buildPed();
  },

  methods : {
    buildPed : function (){

      $('#pedigree').remove();
      $('#pedigrees').append($("<div id='pedigree'></div>"));

      self.opts.dataset = io.readLinkage(self.pedTxt);
      self.opts = ptree.build(self.opts);
    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.Pedigree {
  white-space: pre;
}
</style>
