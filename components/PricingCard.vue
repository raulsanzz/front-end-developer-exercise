<template>
  <div>
   
    <b-container align-v="center" class="container row">
      
        <b-col md="4" v-for="pOptions in pricingOptions" :key="pOptions.id" >
            <b-card-group deck class="mb-3">
            <!-- card 1 -->
            <b-card
              border-variant="default"
              v-bind:header="pOptions.name"
              header-bg-variant="light"
              header-text-variant="dark"
              align="center"
              v-bind:title="'$'+pOptions.cost + '/month'"
              tag="article"
              style="max-width: auto;"
              class="mb-5 mt-2">
              <br />
              <b-list-group flush>
                <b-list-group-item></b-list-group-item>
                <b-list-group-item>
                  <b-icon-check2-circle class="h5 mr-2 mb-0 mt-0" animation="fade"></b-icon-check2-circle>{{pOptions.features[0]}}
                </b-list-group-item>
                <b-list-group-item>
                  <b-icon-x-circle class="h5 mr-2 mb-0 mt-0"></b-icon-x-circle>{{pOptions.features[1]}}
                </b-list-group-item>
                <b-list-group-item>
                  <b-icon-x-circle class="h5 mr-2 mb-0 mt-0"></b-icon-x-circle>{{pOptions.features[2]}}
                </b-list-group-item>
                <b-list-group-item>
                  <b-icon-x-circle class="h5 mr-2 mb-0 mt-0"></b-icon-x-circle>{{pOptions.features[3]}}
                </b-list-group-item>
                <b-list-group-item></b-list-group-item>
              </b-list-group>
              <br />
              <b-button v-b-modal.modal-1 variant="outline-primary" v-on:click="plan = pOptions.name">{{pOptions.cta}}</b-button>
              <br />
            </b-card> 
            </b-card-group>
        </b-col>
      <!-- card 1 ends here-->
    </b-container>
    <b-modal id="modal-1" size="lg" title="New Plan Selected">You have choosen : <b>  {{plan}}</b> </b-modal>
  </div>
</template>

<script>
debugger;
import {mapState} from 'vuex';

export default {
  name: 'PricingCard',
  
  data(){
     return {
       plan:"",  
        
     }
  },
  props: {},
  computed: {
    ...mapState(['pricingOptions'])
  },
  methods: {},
};
</script>
<style lang="scss" scoped>
.card-header { 
  font-size: 1.5rem;
  font-weight: 500;
  line-height: 1.2;
}
.list-group-item {
  border: 0px;
}
.list-group-item {
  padding: 0px;
}
.list-group-flush>.list-group-item {
  color: black;
  font-size: 17px;
  font-weight: 600;
}

</style>
