<template>
    <footer class="">
    <div class="upper-footer">    
        <b-container class="bv-example-row">
            <b-row>
                <b-col>
                <h4 class="titlefooter">KARMA GROUP</h4>
                   <b-row>.
                   <b-col>
                        <h5><a href="https://karmagroup.com/find-destination/" title="Find a Destination">Find a Destination</a></h5>

                        <h5><a href="https://karmagroup.com/karma-experiences/" title="Karma Experiences">Karma Experiences</a></h5>
                        <ul>
                            <li><a href="https://karmagroup.com/inspiration/" title="Inspiration">Inspiration</a></li>
                            <li><a href="https://karmagroup.com/karma-beach/" title="Karma Beach">Karma Beach</a></li>
                            <li><a href="https://karmagroup.com/karma-spa/" title="Karma Spa">Karma Spa</a></li>
                            <li><a href="https://karmagroup.com/karma-boutique/" title="Karma Boutique">Karma Boutique</a></li>
                            <li><a href="https://karmagroup.com/gallery/" title="Image Gallery">Image Gallery</a></li>
                        </ul>
                        <h5><a href="https://karmagroup.com/exclusive-offers/" title="Exclusive Offers">Exclusive Offers</a></h5>
                        <h5><a href="https://karmagroup.com/terms-and-conditions/" title="Terms and Conditions">Terms and Conditions</a></h5>
                        <h5><a href="https://karmagroup.com/privacy-policy/" title="Privacy Policy">Privacy Policy</a></h5>
                        <h5><a href="https://karmagroup.com/app-location-info/" title="App Location Info">App Location Info</a></h5>
                        <h5><a href="https://karmagroup.com/sitemap/" title="Sitemap">Sitemap</a></h5>
                                                                                               </b-col>  
                                                                                                 <b-col>
                         <h5><a href="https://karmagroup.com/news-events/" title="News &amp; Events">News &amp; Events</a></h5>
                          <ul>
                                <li><a href="https://karmagroup.com/awards-accolades/" title="Awards &amp; Accolades">Awards &amp; Accolades</a></li>
                                <li><a href="https://karmagroup.com/karma-curators/" title="Karma Curators">Karma Curators</a></li>
                                <li><a href="https://karmagroup.com/karma-cares/" title="Karma Cares">Karma Cares</a></li>

                                <li><a href="https://karmagroup.com/eventcalendar" title="Events Calendar">Events Calendar</a></li>
                        </ul>

                        <h5><a href="https://karmagroup.com/contact-us/" title="Contact Us">Contact Us</a></h5>
                        <ul>
                        <li><a href="https://karmagroup.com/karma-careers/" title="Careers">Careers</a></li>
                        <li><a href="https://karmagroup.com/media/" title="Media">Media</a></li>
                        <li><a href="https://karmagroup.com/socialmedia/" title="Karma Social">Karma Social</a></li>
                        <li><a href="https://karmagroup.com/gds/" title="GDS Code">GDS Code</a></li>
                        </ul>
                                                                                               </b-col>                                                                       </b-row>
                </b-col>
                <b-col>
                     <h4 class="titlefooter">Newsletter</h4>
                     <div>
    <b-form @submit="onSubmit" @reset="onReset" v-if="show">
    <b-form-group id="group1">
        <b-form-input id="Input1"
                      type="text"
                      v-model="form.name"
                      required
                      placeholder="firstname">
        </b-form-input>
      </b-form-group>
    <b-form-group id="group2">
        <b-form-input id="Input2"
                      type="text"
                      v-model="form.name"
                      required
                      placeholder="lastname">
        </b-form-input>
      </b-form-group>
      <b-form-group id="group3">
        <b-form-input id="Input3"
                      type="email"
                      v-model="form.email"
                      required
                      placeholder="Enter email">
        </b-form-input>
      </b-form-group>
       <b-form-select v-model="selected" class="mb-3" >
      <option :value="null">Please select an option</option>
            <option value="a">Option A</option>
            <option value="b">Option B </option>
            
      </optgroup>
    </b-form-select>

      <b-button type="submit" variant="primary">Submit</b-button>
    </b-form>
  </div>
                </b-col>
                <b-col>
                    <h4 class="titlefooter">Mobile Apps</h4>
                    <img class="phone-image" src="https://karmagroup.com/wp-content/themes/karma/imgs/karma-app-new-screen.png" alt="phone">
                </b-col>
                <b-col>
                    <div class="appdesc">
                        <p class="download-desc">
                          <strong>DOWNLOAD FREE-FLOWING KARMA</strong>
                        </p>

                        <p class="download-icon">
                          <a target="_blank" href="https://play.google.com/store/apps/details?id=com.karmagroups" alt="play store link download">
                            <img class="store-icon" src="https://karmagroup.com/wp-content/themes/karma/imgs/Google-Play.png" alt="play store cta">
                          </a>
                          </p>
                          <p class="download-icon">
                          <a target="_blank" href="https://itunes.apple.com/in/app/karma-resorts/id1296156992?mt=8" alt="app store link download">
                            <img class="store-icon" src="https://karmagroup.com/wp-content/themes/karma/imgs/Apple-app-store.png" alt="app store cta">
                          </a>
                        </p>
                        <p class="desc_app">
                        Put more service &amp; savings in your pocket
                        </p>
                    </div>
                </b-col>
            </b-row>
        </b-container>
    </div>
    <div class="upper-footer"> 
        <b-container class="bv-example-row ">
            <b-row>
                <b-col>col</b-col>
                <b-col>col</b-col>
            </b-row>
        </b-container>
    </div>
    </footer>
</template>

<style scoped>
    footer {
        background: url(https://karmagroup.com/wp-content/themes/karma/imgs/footer-bg.jpg);
        background-size: cover;
    }
    .titlefooter{
            color: #8d7249;
            text-transform:uppercase;
    }
    a{
        text-decoration:none !important;
        color:#ffffff;
    }
    li{
        list-style-type: none;

    }
    .appdesc{
        color:#fff;
        text-align:center;
        position: absolute;
        top: 10%;
    }
</style>


<script>
export default {
  data () {
    return {
      selected: null,
      form: {
        email: '',
        firstname: '',
        lastname: ''       
      },
      foods: [
        { text: 'Select One', value: null },
        'Carrots', 'Beans', 'Tomatoes', 'Corn'
      ],
      show: true
    }
  },
  methods: {
    onSubmit (evt) {
      evt.preventDefault();
      alert(JSON.stringify(this.form));
    },
    onReset (evt) {
      evt.preventDefault();
      /* Reset our form values */
      this.form.email = '';
      this.form.name = '';
      this.form.food = null;
      this.form.checked = [];
      /* Trick to reset/clear native browser form validation state */
      this.show = false;
      this.$nextTick(() => { this.show = true });
    }
  }
}
</script>