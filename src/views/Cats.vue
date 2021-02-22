<template>
  <div>
    <h1>Cats for adoption</h1>
    <b-table striped hover :items="cats">
    <template slot="name" slot-scope="data">
     <router-link :to="`/pets/${data.index}`">
     {{ data.name }} 
     </router-link>
   </template>

    </b-table>
  </div>
</template>

<script>
import {mapState} from 'vuex'
export default {
  data() {
    return {

         }
  },
  computed: {
    ...mapState([
      'cats'
    ])
  }
}
</script>