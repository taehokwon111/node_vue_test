<template>
  <div class="hello">
    <h1>{{ cnt_test }}</h1>
 
  </div>
</template>

<script>
import axios from 'axios';


export default {
  name: 'hello',
  data () {
    return {
      cnt_test: []
    }
  },
  created() {
    	const APIKEY = "dfGEh0ZxCmcCs9D3T70URlxTe77aM%2FAVq%2F47cZb2gRko%2BxANXozELIoiMtAp92ANXucyBoEzbHvcMOYSXzzgDw%3D%3D";
	const dataget = axios({
	  method : 'get',
	  url : 'http://openapi.data.go.kr/openapi/service/rest/Covid19/getCovid19InfStateJson', 
		params: {
		  serviceKey: decodeURIComponent(APIKEY),
		  pageNo: 1,
		  numOfRows: 10,
		  startCreateDt: 20210916,
		  endCreateDt: 20210916
		}
	}).then(r => {
	  
	let a = JSON.stringify(r.data.response.body.items.item.decideCnt);
	let b = JSON.stringify(r.data.response.body.items.item.clearCnt);
	let c = JSON.stringify(r.data.response.body.items.item.deathCnt);
	let d = JSON.stringify(r.data.response.body.items.item.examCnt);

  this.cnt_test = response.data.map(a)
	});
	
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #35495E;
}
</style>
