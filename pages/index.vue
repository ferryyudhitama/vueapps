<template>
  <div>
    <TheHeader />
     <nuxt />
    <div class="main-content">
       <div class="destination">
            <b-container class="bv-example-row">
                 <b-row>
                      <div class="search-wrapper">
                          <input type="text" v-model="keyword" placeholder="Search Destination...">
                      </div>  
                 </b-row>
                 <b-row>                                       
                    <b-col md="4"  v-for="(article, key) in filteredlist" :key="article.title" class="item" >
                        <div class="box">
                          <nuxt-link :to="'/resorts/' + key">{{ article.author }}</nuxt-link>
                        </div>                           
                    </b-col>                                            
                 </b-row>
            </b-container>
       </div>     
    </div>
    <TheFooter />
  </div>
</template>

<style scoped>
  .box{
    min-height: 330px;
    border-radius: 5px;
    background-size: cover;
    margin-top: 30px;
    background-position: center center;
    position: relative;
    background-color: #f9f9f9;
    clear: both;
  }
  .box:hover{
	  -webkit-transform: translateY(-4px);
    -moz-transform: translateY(-4px);
    -o-transform: translateY(-4px);
    -ms-transform: translateY(-4px);
    transform: translateY(-4px);
    -webkit-box-shadow: 0 22px 40px rgba(0, 0, 0, 0.15);
    -moz-box-shadow: 0 22px 40px rgba(0, 0, 0, 0.15);
    box-shadow: 0 22px 40px rgba(0, 0, 0, 0.15);
     -webkit-transition-duration: 0.2s;
    -moz-transition-duration: 0.2s;
    -o-transition-duration: 0.2s;
    transition-duration: 0.2s;

  }
  .main-content{
    background:#eeeeee;
    padding-top: 150px;
    padding-bottom: 150px;
  }
  .destination{
    position: relative;
    top: 12%;
    clear: both;
  }
  .search-wrapper{
    background-color: #fff;
    border-radius: 4px;
    border: 1px solid #bfcbd9;
    color: #1f2d3d;
    display: block;
    font-size: inherit;
    height: 36px;
    line-height: 1;
    padding: 6px 10px 0 10px;
    transition: border-color .2s cubic-bezier(.645,.045,.355,1);
    width: 30%;
    margin: 0 auto;

  }

  .search-wrapper input{
    width:100%;
  }

  textarea:focus, input:focus{
    outline: none;
  }
  
</style>

<script>
  import axios from 'axios'
  import TheHeader from '@/components/TheHeader/TheHeader'
  import TheFooter from '@/components/TheFooter/TheFooter'

  export default {
    components: {
      TheHeader,
      TheFooter
    },

    async asyncData ({ params }) {
      let { data } = await axios.get(`https://newsapi.org/v2/everything?q=bitcoin&apiKey=25a3857fd2194fa1a74eb16ac900b313`)
      // console.log( data );
      return {articles:data.articles}
    },

    // fetch ({ store, params }) {
    //   return axios.get('https://newsapi.org/v2/everything?q=bitcoin&apiKey=25a3857fd2194fa1a74eb16ac900b313')
    //   .then((res) => {
    //     store.commit('setStars', res.data)
    //   })
    // },

    data () {
      return {keyword:''}
    },

    computed: {
      filteredlist() {
        return this.articles.filter((post) => {
          return post.author.includes(this.keyword);
        });
      }


    }
    

  }

</script>