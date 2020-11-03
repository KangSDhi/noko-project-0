<template>
    <div id="Category">
      <div>
        <md-card>
          <md-card-header>
            <md-card-header-text>Sigit</md-card-header-text>
          </md-card-header>
        </md-card>
      </div>
    </div>
</template>

<script>
import axios from 'axios'
import {CATEGORY} from "@/api/ApiEndPoint";

export default {
  name: "Category",
  data(){
    return{
      category: []
    }
  },
  mounted() {
    this.load()
  },
  methods: {
    load(){
      return axios.get(CATEGORY).then(res => {
        console.log(res.data.data)
        this.category = res.data.data
      }).catch((err) => {
        console.log(err)
      })
    }
  }
}
</script>

<style scoped>

</style>