<template>
  <div>
    <TheHeader />
     <nuxt />
    <div class="main-content">
        <div class="desc-resorts">    
            <b-container>   
                <b-card no-body>
                <b-tabs pills card vertical>
                    <b-tab title="Title" active>
                    {{ articles.title }}
                    </b-tab>
                    <b-tab title="Author">
                    {{ articles.author }}
                    </b-tab>
                    <b-tab title="Description">
                    {{ articles.description }}
                    </b-tab>
                </b-tabs>
                </b-card>
            </b-container>
        </div>
    </div>
    <TheFooter />
  </div>
</template>

<style scoped>
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
    //   console.log( data );
    return {articles:data.articles[params.location]}
    }

    

  }

</script>