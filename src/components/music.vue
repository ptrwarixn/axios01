<template>
  <div class="container">
    <input type="text" v-model="keyword"/>
    <button @click="searchData()">Search Artist</button>
<br>
  <b-card-group columns class="roe-m3">
      <b-card v-for="data in resultData" :key="data.artistName"
        :title="data.artistName"       
        img-top
        tag="article"
        style="max-width: 20rem;"
        class="mb-2"
      >
      <br>
     <b-card-text>
        <p>{{data.artistName}}</p>
       <p>{{data.trackName}}</p>
       <a href="#" class="w3-btn w3-black">Link</a>
       </b-card-text>
       
         <br>
      </b-card>
    
  </b-card-group>


  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      resultData: null,
      keyword:'',
    };
  },
  methods: {
    searchData() {
      axios
        .get('https://itunes.apple.com/search?term='+ this.keyword)
        .then((response) => {
          this.resultData = response.data.results;
        //   console.log(response);
        })
        .catch((err) => {
          console.log(err);
        })
    },
  },
};
</script>

<style>

</style>