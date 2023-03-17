<template>
    <span aria-hidden="true" class="wp-block-cover__background has-background-dim-100 has-background-dim">
      
        <div class="entry-content wp-block-post-content has-global-padding is-layout-constrained">
        <div class="wp-duotone-unset-10 wp-block-cover alignwide is-light"
          style="padding-top:2vw;padding-right:4vw;padding-bottom:0;padding-left:4vw;">
          <div class="wp-block-cover__inner-container"> 
            <div class="wp-block-group is-layout-flow wp-container-9">
              <div class="wp-block-group has-global-padding is-layout-constrained wp-container-8">
                <div class="aligncenter is-style-rounded wp-block-site-logo"><img src="roboDoc.ico" class="custom-logo"
                      alt="Predicting and Preventing Health Risks!" decoding="async"
                      srcset="https://probabilisticprevention.files.wordpress.com/2023/03/istockphoto-949119664-612x612-1.jpg?w=132&amp;h=132 132w, https://probabilisticprevention.files.wordpress.com/2023/03/istockphoto-949119664-612x612-1.jpg?w=264&amp;h=264 264w, https://probabilisticprevention.files.wordpress.com/2023/03/istockphoto-949119664-612x612-1.jpg?w=150&amp;h=150 150w"
                      sizes="(max-width: 132px) 100vw, 132px" data-attachment-id="11" data-permalink="roboDoc.ico"
                      data-orig-file="https://probabilisticprevention.files.wordpress.com/2023/03/istockphoto-949119664-612x612-1.jpg"
                      data-orig-size="612,612" data-comments-opened="1"
                      data-image-meta="{&quot;aperture&quot;:&quot;0&quot;,&quot;credit&quot;:&quot;Getty Images\/iStockphoto&quot;,&quot;camera&quot;:&quot;&quot;,&quot;caption&quot;:&quot;Cute white doctor robot. Modern health care. Flat editable vector illustration, clip art&quot;,&quot;created_timestamp&quot;:&quot;0&quot;,&quot;copyright&quot;:&quot;&quot;,&quot;focal_length&quot;:&quot;0&quot;,&quot;iso&quot;:&quot;0&quot;,&quot;shutter_speed&quot;:&quot;0&quot;,&quot;title&quot;:&quot;&quot;,&quot;orientation&quot;:&quot;0&quot;}"
                      data-image-title="istockphoto-949119664-612&#215;612" data-image-description="" data-image-caption="&lt;p&gt;Cute white doctor robot. Modern health care. Flat editable vector illustration, clip art&lt;/p&gt;
  " data-medium-file="https://probabilisticprevention.files.wordpress.com/2023/03/istockphoto-949119664-612x612-1.jpg?w=300"
                      data-large-file="https://probabilisticprevention.files.wordpress.com/2023/03/istockphoto-949119664-612x612-1.jpg?w=612" />
                    </div>
              </div>
              


              <h1 style="font-family: 'Roboto Mono', monospace; font-size:clamp(1.5rem, 1.35rem + ((1vw - 0.48rem) * 0.865), 1.8rem);font-style:normal;font-weight:700;text-transform:capitalize;">Predicting and Preventing
                Health Risks</h1>


                <p>Hey there, health enthusiasts! Welcome to <strong>Probabilistic Prevention</strong> - the web application that helps you assess your risk of developing various diseases. But don't worry, this is <strong>NOT</strong> one of those "WebMD" panic-inducing sites! Instead, we aim to <strong>empower you by providing you with information that could help you make informed decisions about your health</strong>. Our website uses the principles of <strong>conditional probability</strong> to calculate the likelihood of a user having each of 40 diseases. So, let's say you're curious about your chances of developing diabetes or breast cancer - we've got you covered!
<br><br>
Now, you might be wondering, <strong>"How does this work?"</strong> Well, we collect some data from you, including your sex, age, BMI, race, region, smoking level, and physical activity. We know, it sounds like a lot, but these factors are crucial in determining whether someone is prone to certain diseases. Of course, <strong>there are many other factors to consider</strong>, but we've used the most relevant ones based on data from the <strong>CDC, WHO, and National Cancer Institute Databases</strong>. Please note that our calculations are only estimates, and we would have loved to include more data, but we were under time constraints.
<br><br>
So, whether you're a fitness freak or a couch potato, whether you're a salad muncher or a burger lover, our website will provide you with insights on how to <strong>take control of your health</strong>. Remember, "Probabilistic Prevention" is <strong>NOT</strong> a substitute for visiting a doctor or seeking medical advice, but it's a great starting point for taking care of yourself. So, what are you waiting for? Give it a try, and let's see what your probabilities are!</p>
              <hr class="wp-block-separator has-alpha-channel-opacity" />
            </div>
          </div>
          <div data-test='contact-form' id='contact-form-2' class='wp-block-jetpack-contact-form-container '>
              <form onsubmit="return false;" method='' class='contact-form commentsblock wp-block-jetpack-contact-form'>

          <div class="wp-block-jetpack-contact-form" style="padding-top:16px;padding-right:16px;padding-bottom:16px;padding-left:16px">
            <div style="" class='grunion-field-radio-wrap grunion-field-wrap'>
            <h2>Sex</h2>
            <div>
              <input v-model="sex" type="radio" id="male" name="sex" value="male" class='radio  grunion-field'>
              <label for="male">Male</label>

              <input v-model="sex" type="radio" id="female" name="sex" value="female" class='radio  grunion-field'>
              <label for="female">Female</label>
            </div>
          </div>
          </div>
          <div class="wp-block-jetpack-contact-form" style="padding-top:16px;padding-right:16px;padding-bottom:16px;padding-left:16px">
            <div style="" class='grunion-field-name-wrap grunion-field-wrap'>
            <h2>Age</h2>
            <div>
              <dropdown v-model="age" :options="[
                { value: 'ageGroup1', label: '0 - 45' },
                { value: 'ageGroup2', label: '45 - 64' },
                { value: 'ageGroup3', label: '65+' }
              ]" class='name  grunion-field'/>
            </div>
            </div>
          </div>
          <div class="wp-block-jetpack-contact-form" style="padding-top:16px;padding-right:16px;padding-bottom:16px;padding-left:16px">
            <div style="" class='grunion-field-name-wrap grunion-field-wrap'>
            <h2>BMI</h2>
            <div>
              <dropdown v-model="bmi" :options="[
                { value: 'normal', label: 'Normal' },
                { value: 'overweight', label: 'Overweight' },
                { value: 'obese', label: 'Obese' }
              ]" class='name  grunion-field'/>
            </div>
            </div>
          </div>
          <div class="wp-block-jetpack-contact-form" style="padding-top:16px;padding-right:16px;padding-bottom:16px;padding-left:16px">
            <div style="" class='grunion-field-name-wrap grunion-field-wrap'>
            <h2>Race</h2>
            <div>
              <dropdown v-model="race" :options="[
                { value: 'white', label: 'White' },
                { value: 'hispanic', label: 'Hispanic' },
                { value: 'black', label: 'Black' },
                { value: 'asian', label: 'Asian' },
                { value: 'native_pacific_islander', label: 'Native/Pacific Islander' },
                { value: 'native_american', label: 'Native' },
                { value: 'other', label: 'Other' }
              ]" class='name  grunion-field'/>
            </div>
            </div>
          </div>
          <div class="wp-block-jetpack-contact-form" style="padding-top:16px;padding-right:16px;padding-bottom:16px;padding-left:16px">
            <div style="" class='grunion-field-name-wrap grunion-field-wrap'>
            <h2>Region</h2>
            <div>
              <dropdown v-model="region" :options="[
                { value: 'west', label: 'West' },
                { value: 'midwest', label: 'Midwest' },
                { value: 'northeast', label: 'Northeast' },
                { value: 'south', label: 'South' }
              ]" class='name  grunion-field'/>
            </div>
          </div>
          </div>
          <div class="wp-block-jetpack-contact-form" style="padding-top:16px;padding-right:16px;padding-bottom:16px;padding-left:16px">
            <div style="" class='grunion-field-name-wrap grunion-field-wrap'>
            <h2>Smoking Level</h2>
            <div>
              <dropdown v-model="smokerLevel" :options="[
                { value: 'non_smoker', label: 'Non-Smoker' },
                { value: 'occasional_smoker', label: 'Occasional Smoker' },
                { value: 'daily_smoker', label: 'Daily Smoker' },
              ]" class='name  grunion-field'/>
            </div>
            </div>
          </div>
          <div class="wp-block-jetpack-contact-form" style="padding-top:16px;padding-right:16px;padding-bottom:16px;padding-left:16px;">
            <div style="" class='grunion-field-name-wrap grunion-field-wrap'>
            <h2>Physical Activity</h2>
            <div>
              <dropdown v-model="physicalInactivity" :options="[
                { value: 'active', label: 'Active' },
                { value: 'not_active', label: 'Not Active' }
              ]" class='name  grunion-field'/>
            </div>
            </div>
          </div>

          <div class="wp-block-jetpack-button aligncenter wp-block-button">
            <button @click="calculateRisk">
              Calculate Risk
            </button>
            <br>
            <hr class="wp-block-separator has-alpha-channel-opacity" />
          </div>
        </form></div>

          <div v-if="results">
            <h1>Data Processing Here!</h1>
            <div>{{ results }}</div>
          </div>
        </div>
        </div>
    </span>   
</template>
    <!-- Your Vue.js and other scripts go here -->
<script>
import CalculationService from '@/services/CalculationService'


import Dropdown from '@/components/Dropdown'
// import { Bar } from 'vue-chartjs'

export default {
  name: 'App',
  components: {
    Dropdown
  },
  data() {
    return {
      sex: null,
      age: 0,
      bmi: null,
      race: null,
      region: null,
      smokerLevel: null,
      physicalInactivity: null,
      results: null
    }
  },
  computed: {
    convertedSex() {
      return this.sex === 'male' ? 0 : 1
    },
    convertedAge() {
      if (this.age === 'ageGroup1') return 0
      else if (this.age === 'ageGroup2') return 1
      else return 2
    },
    convertedBmi() {
      if (this.bmi === 'normal') return 0
      else if (this.bmi === 'overweight') return 1
      else return 2
    },
    convertedRace() {
      if (this.race === 'white') return 0
      else if (this.race === 'hispanic') return 1
      else if (this.race === 'black') return 2
      else if (this.race === 'other') return 3
      else if (this.race === 'asian') return 4
      else if (this.race === 'native_pacific_islander') return 5
      else return 6
    },
    convertedRegion() {
      if (this.region === 'west') return 0
      else if (this.region === 'midwest') return 1
      else if (this.region === 'northeast') return 2
      else return 3
    },
    convertedSmokerLevel() {
      if (this.smokerLevel === 'non_smoker') return 0
      else if (this.smokerLevel === 'occasional_smoker') return 1
      else return 2
    },
    convertedPhysicalInactivity() {
      if (this.physicalInactivity == 'active') return 1
      else return 0
    },
    isFormValid() {
      return [
        this.sex === null,
        this.age === 0,
        this.bmi === null,
        this.race === null,
        this.region === null,
        this.smokerLevel === null,
        this.physicalInactivity === null,
      ].filter(bool => bool).length === 0
    }
  },
  methods: {
    calculateRisk() {
      this.results = CalculationService.calculateDiseaseProbabilities({
        sex: this.convertedSex,
        age: this.convertedAge,
        bmi: this.convertedBmi,
        race: this.convertedRace,
        region: this.convertedRegion,
        smokerLevel: this.convertedSmokerLevel,
        physicalInactivity: this.convertedPhysicalInactivity,
      })
    }
  }
}
</script>
<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto+Mono&display=swap');

body {
  font-family: 'Roboto Mono', monospace;
  background-color: #BEA7E5;
  margin: 0;
  color: #333;
}
p {
  font-weight: 3em;
}
/* Navigation Bar */
.nav {
  background-color: #424B54;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0.5rem 1rem;
  margin-top: 1em;
  margin-left: 1em;
  margin-right: 1em;
}

.nav img {
  height: 100px;
}

.nav h1 {
  color: white;
  font-size: 24px;
  margin: 0;
  text-align: left;
}

/* Main Content */
#app {
  width: 80%;
  margin: auto;
  padding: 2rem;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  border-color:#0C0CD8; 
  color: #333;
  border-width: 5px;
  font-family: 'Roboto Mono', monospace;
  background-color:#FEFEFE;
  padding-top:var(--wp--preset--spacing--30);
  padding-right:var(--wp--preset--spacing--30);
  padding-bottom:var(--wp--preset--spacing--30);
  padding-left:var(--wp--preset--spacing--30);
  
}

#app img {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: auto;
  flex-direction: column;
  width: 100%;
}
.wp-block-cover__background has-background-dim-100 has-background-dim {
  display: flex;
  justify-content: center;
  align-items: center;
}
h1 {
  font-size: 28px;
  color: #333;
  text-align: center;
  margin-bottom: 2rem;
  
}
strong {
    font-weight: 1000;

}
h2 {
  font-size: 20px;
  font-weight: 1000;
  color: #333;
  margin-bottom: 0.5rem;
}

.input-container {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

.button {
  display: flex;
  justify-content: center;
  align-items: center;
}

input[type="radio"] {
  margin-right: 0.5rem;
}

label {
  margin-right: 1rem;
}

div {
  margin-bottom: 1rem;
}
.wp-block-jetpack-contact-form{
  display:inline-table;
  justify-content:space-between;
  align-items:center;
  margin: 0

}

button {
  background-color: #424B54;
  color: white;
  border: none;
  border-radius: 4px;
  padding: 0.5rem 1rem;
  font-size: 16px;
  cursor: pointer;
  transition: 0.3s;
  margin-top: 1rem;
  margin-bottom: 1rem;
}

button:hover {
  background-color: #353d47;
}
main {
  border-color:#0C0CD8; 
  color: #333;
  border-width: 2px;
  background-color:#F0EFF4;
  border-width:2px;
  padding-top:var(--wp--preset--spacing--30);
  padding-right:var(--wp--preset--spacing--30);
  padding-bottom:var(--wp--preset--spacing--30);
  padding-left:var(--wp--preset--spacing--30);
}

button:disabled {
  background-color: #a7c6ed;
  cursor: not-allowed;
}

hr {
  border: 0;
  height: 1px;
  color: #333;
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.75), rgba(0, 0, 0, 0));
}</style>
 <!-- bullshit styles-->
<style>img.wp-smiley,
img.emoji {
  display: inline !important;
  border: none !important;
  box-shadow: none !important;
  height: 1em !important;
  width: 1em !important;
  margin: 0 0.07em !important;
  vertical-align: -0.1em !important;
  background: none !important;
  padding: 0 !important;
}</style>
   <link crossorigin='anonymous' rel='stylesheet' id='all-css-0-1' href='https://s0.wp.com/_static/??-eJx9jE0SwiAMhS8kjWysLhzPIhRtaiBMA8Xe3rjpQh137+d7D1o2nlMJqUCsJlO9YxJo2XM0EpHC+uE6L7KD3zOpTvyMuSCruzERt3/8yEuYjavOUdB1WSlsOCZPddBYAxiuMqIeSBcxfSOTQNH+4fi5iTd1iWd7sL09He2+n17lsFhd?cssminify=yes' type='text/css' media='all' />
<style id='wp-block-site-logo-inline-css'>.wp-block-site-logo {
  box-sizing: border-box;
  line-height: 0
}

.wp-block-site-logo a {
  display: inline-block
}

.wp-block-site-logo.is-default-size img {
  height: auto;
  width: 120px
}

.wp-block-site-logo img {
  height: auto;
  max-width: 100%
}

.wp-block-site-logo a,
.wp-block-site-logo img {
  border-radius: inherit
}

.wp-block-site-logo.aligncenter {
  margin-left: auto;
  margin-right: auto;
  text-align: center
}

.wp-block-site-logo.is-style-rounded {
  border-radius: 9999px
}

.wp-block-site-logo {
  border-radius: 0;
  border-color: var(--wp--preset--color--primary);
  border-width: 2px;
  border-style: solid;
}</style>
<style id='wp-block-site-title-inline-css'>.wp-block-site-title a {
  color: inherit
}

.wp-block-site-title {
  font-family: var(--wp--preset--font-family--uni-05-53);
  font-size: 0.875rem;
  font-weight: 400;
  text-transform: uppercase;
}

.wp-block-site-title a:where(:not(.wp-element-button)) {
  text-decoration: none;
}</style>
<style id='wp-block-group-inline-css'>.wp-block-group {
  box-sizing: border-box
}</style>
 <link crossorigin='anonymous' rel='stylesheet' id='all-css-6-1' href='https://s0.wp.com/wp-content/plugins/gutenberg-core/v15.3.1/build/block-library/blocks/navigation/style.css?m=1678380765h&cssminify=yes' type='text/css' media='all' />
<style id='wp-block-navigation-inline-css'>.wp-block-navigation {
  font-size: 0.875rem;
  padding-right: 0.25rem !important;
  padding-left: 0.25rem !important;
}

.wp-block-navigation.is-layout-flow>* {
  margin-block-start: 0;
  margin-block-end: 0;
}

.wp-block-navigation.is-layout-flow>*+* {
  margin-block-start: 1rem;
  margin-block-end: 0;
}

.wp-block-navigation.is-layout-constrained>* {
  margin-block-start: 0;
  margin-block-end: 0;
}

.wp-block-navigation.is-layout-constrained>*+* {
  margin-block-start: 1rem;
  margin-block-end: 0;
}

.wp-block-navigation.is-layout-flex {
  gap: 1rem;
}

.wp-block-navigation a:where(:not(.wp-element-button)) {
  color: inherit;
}

.wp-block-navigation a:where(:not(.wp-element-button)):focus {
  text-decoration: underline solid;
}

.wp-block-navigation a:where(:not(.wp-element-button)):active {
  text-decoration: underline dotted;
}</style>
<style id='wp-block-spacer-inline-css'>.wp-block-spacer {
  clear: both
}</style>
<style id='wp-block-post-title-inline-css'>.wp-block-post-title {
  box-sizing: border-box;
  word-break: break-word
}

.wp-block-post-title a {
  display: inline-block
}

.wp-block-post-title {
  font-size: clamp(1.375rem, 1.2916666666666667rem + 0.4166666666666667vw, 1.625rem);
  font-weight: 500;
  margin-bottom: 0;
}

.wp-block-post-title a:where(:not(.wp-element-button)) {
  text-decoration: none;
}</style>
<style id='wp-block-site-tagline-inline-css'>.wp-block-site-tagline {
  font-size: 0.825rem;
}</style>
<style id='wp-block-paragraph-inline-css'>.is-small-text {
  font-size: .875em
}

.is-regular-text {
  font-size: 1em
}

.is-large-text {
  font-size: 2.25em
}

.is-larger-text {
  font-size: 3em
}

.has-drop-cap:not(:focus):first-letter {
  float: left;
  font-size: 8.4em;
  font-style: normal;
  font-weight: 100;
  line-height: .68;
  margin: .05em .1em 0 0;
  text-transform: uppercase
}

body.rtl .has-drop-cap:not(:focus):first-letter {
  float: none;
  margin-left: .1em
}

p.has-drop-cap.has-background {
  overflow: hidden
}

p.has-background {
  padding: 1.25em 2.375em
}

:where(p.has-text-color:not(.has-link-color)) a {
  color: inherit
}</style>
<style id='wp-block-separator-inline-css'>@charset "UTF-8";

.wp-block-separator {
  border: 1px solid;
  border-left: none;
  border-right: none
}

.wp-block-separator.is-style-dots {
  background: none !important;
  border: none;
  height: auto;
  line-height: 1;
  text-align: center
}

.wp-block-separator.is-style-dots:before {
  color: currentColor;
  content: "···";
  font-family: serif;
  font-size: 1.5em;
  letter-spacing: 2em;
  padding-left: 2em
}

.wp-block-separator {
  border-color: currentColor;
  border-width: 0 0 1px 0;
  border-style: solid;
  color: var(--wp--preset--color--foreground);
}</style>
<style id='wp-block-button-inline-css'>.wp-block-button__link {
  box-sizing: border-box;
  cursor: pointer;
  display: inline-block;
  text-align: center;
  word-break: break-word
}

.wp-block-button__link.aligncenter {
  text-align: center
}

.wp-block-button__link.alignright {
  text-align: right
}

:where(.wp-block-button__link) {
  border-radius: 9999px;
  box-shadow: none;
  padding: calc(.667em + 2px) calc(1.333em + 2px);
  text-decoration: none
}

.wp-block-button[style*=text-decoration] .wp-block-button__link {
  text-decoration: inherit
}

.wp-block-buttons>.wp-block-button.has-custom-width {
  max-width: none
}

.wp-block-buttons>.wp-block-button.has-custom-width .wp-block-button__link {
  width: 100%
}

.wp-block-buttons>.wp-block-button.has-custom-font-size .wp-block-button__link {
  font-size: inherit
}

.wp-block-buttons>.wp-block-button.wp-block-button__width-25 {
  width: calc(25% - var(--wp--style--block-gap, .5em)*.75)
}

.wp-block-buttons>.wp-block-button.wp-block-button__width-50 {
  width: calc(50% - var(--wp--style--block-gap, .5em)*.5)
}

.wp-block-buttons>.wp-block-button.wp-block-button__width-75 {
  width: calc(75% - var(--wp--style--block-gap, .5em)*.25)
}

.wp-block-buttons>.wp-block-button.wp-block-button__width-100 {
  flex-basis: 100%;
  width: 100%
}

.wp-block-buttons.is-vertical>.wp-block-button.wp-block-button__width-25 {
  width: 25%
}

.wp-block-buttons.is-vertical>.wp-block-button.wp-block-button__width-50 {
  width: 50%
}

.wp-block-buttons.is-vertical>.wp-block-button.wp-block-button__width-75 {
  width: 75%
}

.wp-block-button.is-style-squared,
.wp-block-button__link.wp-block-button.is-style-squared {
  border-radius: 0
}

.wp-block-button.no-border-radius,
.wp-block-button__link.no-border-radius {
  border-radius: 0 !important
}

.wp-block-button.is-style-outline>.wp-block-button__link,
.wp-block-button .wp-block-button__link.is-style-outline {
  border: 2px solid;
  padding: .667em 1.333em
}

.wp-block-button.is-style-outline>.wp-block-button__link:not(.has-text-color),
.wp-block-button .wp-block-button__link.is-style-outline:not(.has-text-color) {
  color: currentColor
}

.wp-block-button.is-style-outline>.wp-block-button__link:not(.has-background),
.wp-block-button .wp-block-button__link.is-style-outline:not(.has-background) {
  background-color: transparent;
  background-image: none
}

.wp-block-button .wp-block-button__link:where(.has-border-color) {
  border-width: initial
}

.wp-block-button .wp-block-button__link:where([style*=border-top-color]) {
  border-top-width: medium
}

.wp-block-button .wp-block-button__link:where([style*=border-right-color]) {
  border-right-width: medium
}

.wp-block-button .wp-block-button__link:where([style*=border-bottom-color]) {
  border-bottom-width: medium
}

.wp-block-button .wp-block-button__link:where([style*=border-left-color]) {
  border-left-width: medium
}

.wp-block-button .wp-block-button__link:where([style*=border-style]) {
  border-width: initial
}

.wp-block-button .wp-block-button__link:where([style*=border-top-style]) {
  border-top-width: medium
}

.wp-block-button .wp-block-button__link:where([style*=border-right-style]) {
  border-right-width: medium
}

.wp-block-button .wp-block-button__link:where([style*=border-bottom-style]) {
  border-bottom-width: medium
}

.wp-block-button .wp-block-button__link:where([style*=border-left-style]) {
  border-left-width: medium
}</style>
<style id='wp-block-buttons-inline-css'>.wp-block-buttons.is-vertical {
  flex-direction: column
}

.wp-block-buttons.is-vertical>.wp-block-button:last-child {
  margin-bottom: 0
}

.wp-block-buttons>.wp-block-button {
  display: inline-block;
  margin: 0
}

.wp-block-buttons.is-content-justification-left {
  justify-content: flex-start
}

.wp-block-buttons.is-content-justification-left.is-vertical {
  align-items: flex-start
}

.wp-block-buttons.is-content-justification-center {
  justify-content: center
}

.wp-block-buttons.is-content-justification-center.is-vertical {
  align-items: center
}

.wp-block-buttons.is-content-justification-right {
  justify-content: flex-end
}

.wp-block-buttons.is-content-justification-right.is-vertical {
  align-items: flex-end
}

.wp-block-buttons.is-content-justification-space-between {
  justify-content: space-between
}

.wp-block-buttons.aligncenter {
  text-align: center
}

.wp-block-buttons:not(.is-content-justification-space-between, .is-content-justification-right, .is-content-justification-left, .is-content-justification-center) .wp-block-button.aligncenter {
  margin-left: auto;
  margin-right: auto;
  width: 100%
}

.wp-block-buttons[style*=text-decoration] .wp-block-button,
.wp-block-buttons[style*=text-decoration] .wp-block-button__link {
  text-decoration: inherit
}

.wp-block-buttons.has-custom-font-size .wp-block-button__link {
  font-size: inherit
}

.wp-block-button.aligncenter {
  text-align: center
}</style>
 <link crossorigin='anonymous' rel='stylesheet' id='all-css-22-1' href='https://s0.wp.com/_static/??-eJyVjt0OgjAMRl/I0SxEwQvjoxhW6jLcD+k6CG/viHLllXf9+rUnB9ZZYYpCUSAUNftiXcwwkcwDvr4ZZk5jQXEpwsNFBOMTvjKYIlJXi6O1wZxP8C8s1MlThv1pQFHPxAEqCSyXWA9+qAfSlhoNsa0NEyz63LSNrkLOjx875Z3hgbfDFdNCDFk2Tzv1Hm760vVtf+1aPb0BbgZhlw==?cssminify=yes' type='text/css' media='all' />
<style id='wp-block-post-content-inline-css'>.wp-block-post-content.is-layout-flow>* {
  margin-block-start: 0;
  margin-block-end: 0;
}

.wp-block-post-content.is-layout-flow>*+* {
  margin-block-start: var(--wp--custom--gap--vertical);
  margin-block-end: 0;
}

.wp-block-post-content.is-layout-constrained>* {
  margin-block-start: 0;
  margin-block-end: 0;
}

.wp-block-post-content.is-layout-constrained>*+* {
  margin-block-start: var(--wp--custom--gap--vertical);
  margin-block-end: 0;
}

.wp-block-post-content.is-layout-flex {
  gap: var(--wp--custom--gap--vertical);
}

.wp-block-post-content a:where(:not(.wp-element-button)):hover {
  font-style: italic;
}

.wp-block-post-content a:where(:not(.wp-element-button)):focus {
  font-style: italic;
}

.wp-block-post-content a:where(:not(.wp-element-button)):active {
  font-style: italic;
}</style>
<style id='wp-block-post-terms-inline-css'>.wp-block-post-terms {
  box-sizing: border-box
}

.wp-block-post-terms .wp-block-post-terms__separator {
  white-space: pre-wrap
}</style>
<style id='wp-block-library-inline-css'>:root {
  --wp-admin-theme-color: #007cba;
  --wp-admin-theme-color--rgb: 0, 124, 186;
  --wp-admin-theme-color-darker-10: #006ba1;
  --wp-admin-theme-color-darker-10--rgb: 0, 107, 161;
  --wp-admin-theme-color-darker-20: #005a87;
  --wp-admin-theme-color-darker-20--rgb: 0, 90, 135;
  --wp-admin-border-width-focus: 2px;
  --wp-block-synced-color: #7a00df;
  --wp-block-synced-color--rgb: 122, 0, 223
}

@media (-webkit-min-device-pixel-ratio:2),
(min-resolution:192dpi) {
  :root {
    --wp-admin-border-width-focus: 1.5px
  }
}

.wp-element-button {
  cursor: pointer
}

:root {
  --wp--preset--font-size--normal: 16px;
  --wp--preset--font-size--huge: 42px
}

:root .has-very-light-gray-background-color {
  background-color: #eee
}

:root .has-very-dark-gray-background-color {
  background-color: #313131
}

:root .has-very-light-gray-color {
  color: #eee
}

:root .has-very-dark-gray-color {
  color: #313131
}

:root .has-vivid-green-cyan-to-vivid-cyan-blue-gradient-background {
  background: linear-gradient(135deg, #00d084, #0693e3)
}

:root .has-purple-crush-gradient-background {
  background: linear-gradient(135deg, #34e2e4, #4721fb 50%, #ab1dfe)
}

:root .has-hazy-dawn-gradient-background {
  background: linear-gradient(135deg, #faaca8, #dad0ec)
}

:root .has-subdued-olive-gradient-background {
  background: linear-gradient(135deg, #fafae1, #67a671)
}

:root .has-atomic-cream-gradient-background {
  background: linear-gradient(135deg, #fdd79a, #004a59)
}

:root .has-nightshade-gradient-background {
  background: linear-gradient(135deg, #330968, #31cdcf)
}

:root .has-midnight-gradient-background {
  background: linear-gradient(135deg, #020381, #2874fc)
}

.has-regular-font-size {
  font-size: 1em
}

.has-larger-font-size {
  font-size: 2.625em
}

.has-normal-font-size {
  font-size: var(--wp--preset--font-size--normal)
}

.has-huge-font-size {
  font-size: var(--wp--preset--font-size--huge)
}

.has-text-align-center {
  text-align: center
}

.has-text-align-left {
  text-align: left
}

.has-text-align-right {
  text-align: right
}

#end-resizable-editor-section {
  display: none
}

.aligncenter {
  clear: both
}

.items-justified-left {
  justify-content: flex-start
}

.items-justified-center {
  justify-content: center
}

.items-justified-right {
  justify-content: flex-end
}

.items-justified-space-between {
  justify-content: space-between
}

.screen-reader-text {
  clip: rect(1px, 1px, 1px, 1px);
  word-wrap: normal !important;
  border: 0;
  -webkit-clip-path: inset(50%);
  clip-path: inset(50%);
  height: 1px;
  margin: -1px;
  overflow: hidden;
  padding: 0;
  position: absolute;
  width: 1px
}

.screen-reader-text:focus {
  clip: auto !important;
  background-color: #ddd;
  -webkit-clip-path: none;
  clip-path: none;
  color: #444;
  display: block;
  font-size: 1em;
  height: auto;
  left: 5px;
  line-height: normal;
  padding: 15px 23px 14px;
  text-decoration: none;
  top: 5px;
  width: auto;
  z-index: 100000
}

html :where(.has-border-color) {
  border-style: solid
}

html :where([style*=border-top-color]) {
  border-top-style: solid
}

html :where([style*=border-right-color]) {
  border-right-style: solid
}

html :where([style*=border-bottom-color]) {
  border-bottom-style: solid
}

html :where([style*=border-left-color]) {
  border-left-style: solid
}

html :where([style*=border-width]) {
  border-style: solid
}

html :where([style*=border-top-width]) {
  border-top-style: solid
}

html :where([style*=border-right-width]) {
  border-right-style: solid
}

html :where([style*=border-bottom-width]) {
  border-bottom-style: solid
}

html :where([style*=border-left-width]) {
  border-left-style: solid
}

html :where(img[class*=wp-image-]) {
  height: auto;
  max-width: 100%
}

figure {
  margin: 0 0 1em
}

html :where(.is-position-sticky) {
  --wp-admin--admin-bar--position-offset: var(--wp-admin--admin-bar--height, 0px)
}

@media screen and (max-width:600px) {
  html :where(.is-position-sticky) {
    --wp-admin--admin-bar--position-offset: 0px
  }
}

.has-text-align-justify {
  text-align: justify;
}

.wp-block-cover__image-background.has-parallax {
  background-size: cover;
}</style>
 <link crossorigin='anonymous' rel='stylesheet' id='all-css-30-1' href='https://s0.wp.com/_static/??-eJx9jUEOwjAMBD+EMbRSOCHekqRWMaqTKHbU7zdQqaeKi7W2d3ZxLRBzMkqG0qAsbeak6CfhBMFXXEvMAsd+jaoXZEzZuHN6iP1xnhZzpX6X4u3rEJrY00LSbf+wvTqEUkkV+hRuAvbu4K/uJc+7ezg3DONt/GwPtEqR?cssminify=yes' type='text/css' media='all' />
<style id='wpcom-admin-bar-inline-css'>.admin-bar {
  position: inherit !important;
  top: auto !important;
}

.admin-bar .goog-te-banner-frame {
  top: 32px !important
}

@media screen and (max-width: 782px) {
  .admin-bar .goog-te-banner-frame {
    top: 46px !important;
  }
}

@media screen and (max-width: 480px) {
  .admin-bar .goog-te-banner-frame {
    position: absolute;
  }
}</style>
<style id='global-styles-inline-css'>body {
  --wp--preset--color--black: #000000;
  --wp--preset--color--cyan-bluish-gray: #abb8c3;
  --wp--preset--color--white: #ffffff;
  --wp--preset--color--pale-pink: #f78da7;
  --wp--preset--color--vivid-red: #cf2e2e;
  --wp--preset--color--luminous-vivid-orange: #ff6900;
  --wp--preset--color--luminous-vivid-amber: #fcb900;
  --wp--preset--color--light-green-cyan: #7bdcb5;
  --wp--preset--color--vivid-green-cyan: #00d084;
  --wp--preset--color--pale-cyan-blue: #8ed1fc;
  --wp--preset--color--vivid-cyan-blue: #0693e3;
  --wp--preset--color--vivid-purple: #9b51e0;
  --wp--preset--color--primary: #040DE1;
  --wp--preset--color--foreground: #040DE1;
  --wp--preset--color--background: #DDCFFF;
  --wp--preset--color--tertiary: #CDBAF9;
  --wp--preset--gradient--vivid-cyan-blue-to-vivid-purple: linear-gradient(135deg, rgba(6, 147, 227, 1) 0%, rgb(155, 81, 224) 100%);
  --wp--preset--gradient--light-green-cyan-to-vivid-green-cyan: linear-gradient(135deg, rgb(122, 220, 180) 0%, rgb(0, 208, 130) 100%);
  --wp--preset--gradient--luminous-vivid-amber-to-luminous-vivid-orange: linear-gradient(135deg, rgba(252, 185, 0, 1) 0%, rgba(255, 105, 0, 1) 100%);
  --wp--preset--gradient--luminous-vivid-orange-to-vivid-red: linear-gradient(135deg, rgba(255, 105, 0, 1) 0%, rgb(207, 46, 46) 100%);
  --wp--preset--gradient--very-light-gray-to-cyan-bluish-gray: linear-gradient(135deg, rgb(238, 238, 238) 0%, rgb(169, 184, 195) 100%);
  --wp--preset--gradient--cool-to-warm-spectrum: linear-gradient(135deg, rgb(74, 234, 220) 0%, rgb(151, 120, 209) 20%, rgb(207, 42, 186) 40%, rgb(238, 44, 130) 60%, rgb(251, 105, 98) 80%, rgb(254, 248, 76) 100%);
  --wp--preset--gradient--blush-light-purple: linear-gradient(135deg, rgb(255, 206, 236) 0%, rgb(152, 150, 240) 100%);
  --wp--preset--gradient--blush-bordeaux: linear-gradient(135deg, rgb(254, 205, 165) 0%, rgb(254, 45, 45) 50%, rgb(107, 0, 62) 100%);
  --wp--preset--gradient--luminous-dusk: linear-gradient(135deg, rgb(255, 203, 112) 0%, rgb(199, 81, 192) 50%, rgb(65, 88, 208) 100%);
  --wp--preset--gradient--pale-ocean: linear-gradient(135deg, rgb(255, 245, 203) 0%, rgb(182, 227, 212) 50%, rgb(51, 167, 181) 100%);
  --wp--preset--gradient--electric-grass: linear-gradient(135deg, rgb(202, 248, 128) 0%, rgb(113, 206, 126) 100%);
  --wp--preset--gradient--midnight: linear-gradient(135deg, rgb(2, 3, 129) 0%, rgb(40, 116, 252) 100%);
  --wp--preset--duotone--dark-grayscale: url('#wp-duotone-dark-grayscale');
  --wp--preset--duotone--grayscale: url('#wp-duotone-grayscale');
  --wp--preset--duotone--purple-yellow: url('#wp-duotone-purple-yellow');
  --wp--preset--duotone--blue-red: url('#wp-duotone-blue-red');
  --wp--preset--duotone--midnight: url('#wp-duotone-midnight');
  --wp--preset--duotone--magenta-yellow: url('#wp-duotone-magenta-yellow');
  --wp--preset--duotone--purple-green: url('#wp-duotone-purple-green');
  --wp--preset--duotone--blue-orange: url('#wp-duotone-blue-orange');
  --wp--preset--font-size--small: .813rem;
  --wp--preset--font-size--medium: clamp(1rem, 1rem + ((1vw - 0.48rem) * 0.24), 1.125rem);
  --wp--preset--font-size--large: 1.5rem;
  --wp--preset--font-size--x-large: 2rem;
  --wp--preset--font-family--dm-mono: 'DM Mono', sans-serif;
  --wp--preset--font-family--uni-05-53: 'uni 05_53', sans-serif;
  --wp--preset--font-family--albert-sans: 'Albert Sans';
  --wp--preset--font-family--alegreya: Alegreya;
  --wp--preset--font-family--arvo: Arvo;
  --wp--preset--font-family--bodoni-moda: 'Bodoni Moda';
  --wp--preset--font-family--cabin: Cabin;
  --wp--preset--font-family--chivo: Chivo;
  --wp--preset--font-family--commissioner: Commissioner;
  --wp--preset--font-family--cormorant: Cormorant;
  --wp--preset--font-family--courier-prime: 'Courier Prime';
  --wp--preset--font-family--crimson-pro: 'Crimson Pro';
  --wp--preset--font-family--dm-sans: 'DM Sans';
  --wp--preset--font-family--domine: Domine;
  --wp--preset--font-family--eb-garamond: 'EB Garamond';
  --wp--preset--font-family--epilogue: Epilogue;
  --wp--preset--font-family--figtree: Figtree;
  --wp--preset--font-family--fira-sans: 'Fira Sans';
  --wp--preset--font-family--fraunces: Fraunces;
  --wp--preset--font-family--ibm-plex-mono: 'IBM Plex Mono';
  --wp--preset--font-family--ibm-plex-sans: 'IBM Plex Sans';
  --wp--preset--font-family--inter: Inter;
  --wp--preset--font-family--josefin-sans: 'Josefin Sans';
  --wp--preset--font-family--jost: Jost;
  --wp--preset--font-family--libre-baskerville: 'Libre Baskerville';
  --wp--preset--font-family--libre-franklin: 'Libre Franklin';
  --wp--preset--font-family--literata: Literata;
  --wp--preset--font-family--lora: Lora;
  --wp--preset--font-family--merriweather: Merriweather;
  --wp--preset--font-family--montserrat: Montserrat;
  --wp--preset--font-family--newsreader: Newsreader;
  --wp--preset--font-family--nunito: Nunito;
  --wp--preset--font-family--open-sans: 'Open Sans';
  --wp--preset--font-family--overpass: Overpass;
  --wp--preset--font-family--petrona: Petrona;
  --wp--preset--font-family--piazzolla: Piazzolla;
  --wp--preset--font-family--playfair-display: 'Playfair Display';
  --wp--preset--font-family--plus-jakarta-sans: 'Plus Jakarta Sans';
  --wp--preset--font-family--poppins: Poppins;
  --wp--preset--font-family--raleway: Raleway;
  --wp--preset--font-family--roboto-slab: 'Roboto Slab';
  --wp--preset--font-family--roboto: Roboto;
  --wp--preset--font-family--rubik: Rubik;
  --wp--preset--font-family--sora: Sora;
  --wp--preset--font-family--source-sans-pro: 'Source Sans Pro';
  --wp--preset--font-family--source-serif-pro: 'Source Serif Pro';
  --wp--preset--font-family--space-mono: 'Space Mono';
  --wp--preset--font-family--texturina: Texturina;
  --wp--preset--font-family--work-sans: 'Work Sans';
  --wp--preset--spacing--20: 0.44rem;
  --wp--preset--spacing--30: 0.67rem;
  --wp--preset--spacing--40: 1rem;
  --wp--preset--spacing--50: 1.5rem;
  --wp--preset--spacing--60: 2.25rem;
  --wp--preset--spacing--70: 3.38rem;
  --wp--preset--spacing--80: 5.06rem;
  --wp--preset--shadow--natural: 6px 6px 9px rgba(0, 0, 0, 0.2);
  --wp--preset--shadow--deep: 12px 12px 50px rgba(0, 0, 0, 0.4);
  --wp--preset--shadow--sharp: 6px 6px 0px rgba(0, 0, 0, 0.2);
  --wp--preset--shadow--outlined: 6px 6px 0px -3px rgba(255, 255, 255, 1), 6px 6px rgba(0, 0, 0, 1);
  --wp--preset--shadow--crisp: 6px 6px 0px rgba(0, 0, 0, 1);
  --wp--custom--gap--horizontal: min(30px, 5vw);
  --wp--custom--gap--vertical: min(30px, 5vw);
  --wp--custom--spacing--outer: clamp(0.625rem, calc(0.625rem + ((1vw - 0.48rem) * 1.2019)), 1.25rem);
  --wp--custom--shadow: 5px 5px 0px -2px var(--wp--preset--color--background), 5px 5px var(--wp--preset--color--foreground);
}

body {
  margin: 0;
  --wp--style--global--content-size: 620px;
  --wp--style--global--wide-size: 1200px;
}

.wp-site-blocks {
  padding-top: 1em;
  margin-bottom: 0em;
}

.has-global-padding {
  padding-right: var(--wp--style--root--padding-right);
  padding-left: var(--wp--style--root--padding-left);
}

.has-global-padding :where(.has-global-padding) {
  padding-right: 0;
  padding-left: 0;
}

.has-global-padding>.alignfull {
  margin-right: calc(var(--wp--style--root--padding-right) * -1);
  margin-left: calc(var(--wp--style--root--padding-left) * -1);
}

.has-global-padding :where(.has-global-padding)>.alignfull {
  margin-right: 0;
  margin-left: 0;
}

.has-global-padding>.alignfull:where(:not(.has-global-padding))> :where([class*="wp-block-"]:not(.alignfull):not([class*="__"]), .wp-block:not(.alignfull), p, h1, h2, h3, h4, h5, h6, ul, ol) {
  padding-right: var(--wp--style--root--padding-right);
  padding-left: var(--wp--style--root--padding-left);
}

.has-global-padding :where(.has-global-padding)>.alignfull:where(:not(.has-global-padding))> :where([class*="wp-block-"]:not(.alignfull):not([class*="__"]), .wp-block:not(.alignfull), p, h1, h2, h3, h4, h5, h6, ul, ol) {
  padding-right: 0;
  padding-left: 0;
}

.wp-site-blocks>.alignleft {
  float: left;
  margin-right: 2em;
}

.wp-site-blocks>.alignright {
  float: right;
  margin-left: 2em;
}

.wp-site-blocks>.aligncenter {
  justify-content: center;
  margin-left: auto;
  margin-right: auto;
}

.wp-site-blocks>* {
  margin-block-start: 0;
  margin-block-end: 0;
}

.wp-site-blocks>*+* {
  margin-block-start: var(--wp--custom--gap--vertical);
}

body {
  --wp--style--block-gap: var(--wp--custom--gap--vertical);
}

body .is-layout-flow>* {
  margin-block-start: 0;
  margin-block-end: 0;
}

body .is-layout-flow>*+* {
  margin-block-start: var(--wp--custom--gap--vertical);
  margin-block-end: 0;
}

body .is-layout-constrained>* {
  margin-block-start: 0;
  margin-block-end: 0;
}

body .is-layout-constrained>*+* {
  margin-block-start: var(--wp--custom--gap--vertical);
  margin-block-end: 0;
}

body .is-layout-flex {
  gap: var(--wp--custom--gap--vertical);
}

body .is-layout-flow>.alignleft {
  float: left;
  margin-inline-start: 0;
  margin-inline-end: 2em;
}

body .is-layout-flow>.alignright {
  float: right;
  margin-inline-start: 2em;
  margin-inline-end: 0;
}

body .is-layout-flow>.aligncenter {
  margin-left: auto !important;
  margin-right: auto !important;
}

body .is-layout-constrained>.alignleft {
  float: left;
  margin-inline-start: 0;
  margin-inline-end: 2em;
}

body .is-layout-constrained>.alignright {
  float: right;
  margin-inline-start: 2em;
  margin-inline-end: 0;
}

body .is-layout-constrained>.aligncenter {
  margin-left: auto !important;
  margin-right: auto !important;
}

body .is-layout-constrained> :where(:not(.alignleft):not(.alignright):not(.alignfull)) {
  max-width: var(--wp--style--global--content-size);
  margin-left: auto !important;
  margin-right: auto !important;
}

body .is-layout-constrained>.alignwide {
  max-width: var(--wp--style--global--wide-size);
}

body .is-layout-flex {
  display: flex;
}

body .is-layout-flex {
  flex-wrap: wrap;
  align-items: center;
}

body .is-layout-flex>* {
  margin: 0;
}

body {
  background-color: var(--wp--preset--color--background);
  color: var(--wp--preset--color--foreground);
  font-family: var(--wp--preset--font-family--dm-mono);
  font-size: 0.875rem;
  font-weight: 300;
  line-height: 1.6;
  --wp--style--root--padding-top: var(--wp--custom--spacing--outer);
  --wp--style--root--padding-right: var(--wp--custom--spacing--outer);
  --wp--style--root--padding-bottom: var(--wp--custom--spacing--outer);
  --wp--style--root--padding-left: var(--wp--custom--spacing--outer);
}

a:where(:not(.wp-element-button)) {
  color: var(--wp--preset--color--primary);
  text-decoration: underline;
}

a:where(:not(.wp-element-button)):hover {
  text-decoration: underline dotted;
}

a:where(:not(.wp-element-button)):focus {
  text-decoration: underline dotted;
}

a:where(:not(.wp-element-button)):active {
  text-decoration: underline solid;
}

h1,
h2,
h3,
h4,
h5,
h6 {
  font-weight: 500;
  letter-spacing: 0.05em;
  line-height: 1.2;
}

h1 {
  font-size: clamp(1.375rem, 1.1442307692307692rem + 0.4807692307692308vw, 1.625rem);
}

h2 {
  font-size: clamp(1.25rem, 1.1346153846153846rem + 0.2403846153846154vw, 1.375rem);
}

h3 {
  font-size: clamp(1.125rem, 1.0096153846153846rem + 0.2403846153846154vw, 1.25rem);
}

h4 {
  font-size: clamp(0.875rem, 0.875rem + ((1vw - 0.48rem) * 0.481), 1.125rem);
}

h5 {
  font-size: 0.813rem;
  text-transform: uppercase;
}

h6 {
  font-size: 0.75rem;
  font-weight: 400;
  line-height: 1.6;
  text-transform: uppercase;
}

.wp-element-button,
.wp-block-button__link {
  background-color: var(--wp--preset--color--primary);
  border-radius: 0;
  border-color: var(--wp--preset--color--primary);
  border-width: 2px;
  border-style: solid;
  color: var(--wp--preset--color--background);
  font-family: inherit;
  font-size: var(--wp--preset--font-size--small);
  line-height: inherit;
  padding-top: calc(0.75em - 2px);
  padding-right: calc(1.5em - 2px);
  padding-bottom: calc(0.75em - 2px);
  padding-left: calc(1.5em - 2px);
  text-decoration: none;
  box-shadow: var(--wp--custom--shadow) !important;
}

.wp-element-button,
.wp-block-button__link:hover {
  background-color: var(--wp--preset--color--background);
  border-color: var(--wp--preset--color--primary);
  color: var(--wp--preset--color--primary);
}

.wp-element-button,
.wp-block-button__link:active {
  background-color: var(--wp--preset--color--primary);
  border-color: var(--wp--preset--color--primary);
  color: var(--wp--preset--color--background);
  box-shadow: 2px 2px var(--wp--preset--color--primary) !important;
}

.has-black-color {
  color: var(--wp--preset--color--black) !important;
}

.has-cyan-bluish-gray-color {
  color: var(--wp--preset--color--cyan-bluish-gray) !important;
}

.has-white-color {
  color: var(--wp--preset--color--white) !important;
}

.has-pale-pink-color {
  color: var(--wp--preset--color--pale-pink) !important;
}

.has-vivid-red-color {
  color: var(--wp--preset--color--vivid-red) !important;
}

.has-luminous-vivid-orange-color {
  color: var(--wp--preset--color--luminous-vivid-orange) !important;
}

.has-luminous-vivid-amber-color {
  color: var(--wp--preset--color--luminous-vivid-amber) !important;
}

.has-light-green-cyan-color {
  color: var(--wp--preset--color--light-green-cyan) !important;
}

.has-vivid-green-cyan-color {
  color: var(--wp--preset--color--vivid-green-cyan) !important;
}

.has-pale-cyan-blue-color {
  color: var(--wp--preset--color--pale-cyan-blue) !important;
}

.has-vivid-cyan-blue-color {
  color: var(--wp--preset--color--vivid-cyan-blue) !important;
}

.has-vivid-purple-color {
  color: var(--wp--preset--color--vivid-purple) !important;
}

.has-primary-color {
  color: var(--wp--preset--color--primary) !important;
}

.has-foreground-color {
  color: var(--wp--preset--color--foreground) !important;
}

.has-background-color {
  color: var(--wp--preset--color--background) !important;
}

.has-tertiary-color {
  color: var(--wp--preset--color--tertiary) !important;
}

.has-black-background-color {
  background-color: var(--wp--preset--color--black) !important;
}

.has-cyan-bluish-gray-background-color {
  background-color: var(--wp--preset--color--cyan-bluish-gray) !important;
}

.has-white-background-color {
  background-color: var(--wp--preset--color--white) !important;
}

.has-pale-pink-background-color {
  background-color: var(--wp--preset--color--pale-pink) !important;
}

.has-vivid-red-background-color {
  background-color: var(--wp--preset--color--vivid-red) !important;
}

.has-luminous-vivid-orange-background-color {
  background-color: var(--wp--preset--color--luminous-vivid-orange) !important;
}

.has-luminous-vivid-amber-background-color {
  background-color: var(--wp--preset--color--luminous-vivid-amber) !important;
}

.has-light-green-cyan-background-color {
  background-color: var(--wp--preset--color--light-green-cyan) !important;
}

.has-vivid-green-cyan-background-color {
  background-color: var(--wp--preset--color--vivid-green-cyan) !important;
}

.has-pale-cyan-blue-background-color {
  background-color: var(--wp--preset--color--pale-cyan-blue) !important;
}

.has-vivid-cyan-blue-background-color {
  background-color: var(--wp--preset--color--vivid-cyan-blue) !important;
}

.has-vivid-purple-background-color {
  background-color: var(--wp--preset--color--vivid-purple) !important;
}

.has-primary-background-color {
  background-color: var(--wp--preset--color--primary) !important;
}

.has-foreground-background-color {
  background-color: var(--wp--preset--color--foreground) !important;
}

.has-background-background-color {
  background-color: var(--wp--preset--color--background) !important;
}

.has-tertiary-background-color {
  background-color: var(--wp--preset--color--tertiary) !important;
}

.has-black-border-color {
  border-color: var(--wp--preset--color--black) !important;
}

.has-cyan-bluish-gray-border-color {
  border-color: var(--wp--preset--color--cyan-bluish-gray) !important;
}

.has-white-border-color {
  border-color: var(--wp--preset--color--white) !important;
}

.has-pale-pink-border-color {
  border-color: var(--wp--preset--color--pale-pink) !important;
}

.has-vivid-red-border-color {
  border-color: var(--wp--preset--color--vivid-red) !important;
}

.has-luminous-vivid-orange-border-color {
  border-color: var(--wp--preset--color--luminous-vivid-orange) !important;
}

.has-luminous-vivid-amber-border-color {
  border-color: var(--wp--preset--color--luminous-vivid-amber) !important;
}

.has-light-green-cyan-border-color {
  border-color: var(--wp--preset--color--light-green-cyan) !important;
}

.has-vivid-green-cyan-border-color {
  border-color: var(--wp--preset--color--vivid-green-cyan) !important;
}

.has-pale-cyan-blue-border-color {
  border-color: var(--wp--preset--color--pale-cyan-blue) !important;
}

.has-vivid-cyan-blue-border-color {
  border-color: var(--wp--preset--color--vivid-cyan-blue) !important;
}

.has-vivid-purple-border-color {
  border-color: var(--wp--preset--color--vivid-purple) !important;
}

.has-primary-border-color {
  border-color: var(--wp--preset--color--primary) !important;
}

.has-foreground-border-color {
  border-color: var(--wp--preset--color--foreground) !important;
}

.has-background-border-color {
  border-color: var(--wp--preset--color--background) !important;
}

.has-tertiary-border-color {
  border-color: var(--wp--preset--color--tertiary) !important;
}

.has-vivid-cyan-blue-to-vivid-purple-gradient-background {
  background: var(--wp--preset--gradient--vivid-cyan-blue-to-vivid-purple) !important;
}

.has-light-green-cyan-to-vivid-green-cyan-gradient-background {
  background: var(--wp--preset--gradient--light-green-cyan-to-vivid-green-cyan) !important;
}

.has-luminous-vivid-amber-to-luminous-vivid-orange-gradient-background {
  background: var(--wp--preset--gradient--luminous-vivid-amber-to-luminous-vivid-orange) !important;
}

.has-luminous-vivid-orange-to-vivid-red-gradient-background {
  background: var(--wp--preset--gradient--luminous-vivid-orange-to-vivid-red) !important;
}

.has-very-light-gray-to-cyan-bluish-gray-gradient-background {
  background: var(--wp--preset--gradient--very-light-gray-to-cyan-bluish-gray) !important;
}

.has-cool-to-warm-spectrum-gradient-background {
  background: var(--wp--preset--gradient--cool-to-warm-spectrum) !important;
}

.has-blush-light-purple-gradient-background {
  background: var(--wp--preset--gradient--blush-light-purple) !important;
}

.has-blush-bordeaux-gradient-background {
  background: var(--wp--preset--gradient--blush-bordeaux) !important;
}

.has-luminous-dusk-gradient-background {
  background: var(--wp--preset--gradient--luminous-dusk) !important;
}

.has-pale-ocean-gradient-background {
  background: var(--wp--preset--gradient--pale-ocean) !important;
}

.has-electric-grass-gradient-background {
  background: var(--wp--preset--gradient--electric-grass) !important;
}

.has-midnight-gradient-background {
  background: var(--wp--preset--gradient--midnight) !important;
}

.has-small-font-size {
  font-size: var(--wp--preset--font-size--small) !important;
}

.has-medium-font-size {
  font-size: var(--wp--preset--font-size--medium) !important;
}

.has-large-font-size {
  font-size: var(--wp--preset--font-size--large) !important;
}

.has-x-large-font-size {
  font-size: var(--wp--preset--font-size--x-large) !important;
}

.has-dm-mono-font-family {
  font-family: var(--wp--preset--font-family--dm-mono) !important;
}

.has-uni-05-53-font-family {
  font-family: var(--wp--preset--font-family--uni-05-53) !important;
}

.has-albert-sans-font-family {
  font-family: var(--wp--preset--font-family--albert-sans) !important;
}

.has-alegreya-font-family {
  font-family: var(--wp--preset--font-family--alegreya) !important;
}

.has-arvo-font-family {
  font-family: var(--wp--preset--font-family--arvo) !important;
}

.has-bodoni-moda-font-family {
  font-family: var(--wp--preset--font-family--bodoni-moda) !important;
}

.has-cabin-font-family {
  font-family: var(--wp--preset--font-family--cabin) !important;
}

.has-chivo-font-family {
  font-family: var(--wp--preset--font-family--chivo) !important;
}

.has-commissioner-font-family {
  font-family: var(--wp--preset--font-family--commissioner) !important;
}

.has-cormorant-font-family {
  font-family: var(--wp--preset--font-family--cormorant) !important;
}

.has-courier-prime-font-family {
  font-family: var(--wp--preset--font-family--courier-prime) !important;
}

.has-crimson-pro-font-family {
  font-family: var(--wp--preset--font-family--crimson-pro) !important;
}

.has-dm-sans-font-family {
  font-family: var(--wp--preset--font-family--dm-sans) !important;
}

.has-domine-font-family {
  font-family: var(--wp--preset--font-family--domine) !important;
}

.has-eb-garamond-font-family {
  font-family: var(--wp--preset--font-family--eb-garamond) !important;
}

.has-epilogue-font-family {
  font-family: var(--wp--preset--font-family--epilogue) !important;
}

.has-figtree-font-family {
  font-family: var(--wp--preset--font-family--figtree) !important;
}

.has-fira-sans-font-family {
  font-family: var(--wp--preset--font-family--fira-sans) !important;
}

.has-fraunces-font-family {
  font-family: var(--wp--preset--font-family--fraunces) !important;
}

.has-ibm-plex-mono-font-family {
  font-family: var(--wp--preset--font-family--ibm-plex-mono) !important;
}

.has-ibm-plex-sans-font-family {
  font-family: var(--wp--preset--font-family--ibm-plex-sans) !important;
}

.has-inter-font-family {
  font-family: var(--wp--preset--font-family--inter) !important;
}

.has-josefin-sans-font-family {
  font-family: var(--wp--preset--font-family--josefin-sans) !important;
}

.has-jost-font-family {
  font-family: var(--wp--preset--font-family--jost) !important;
}

.has-libre-baskerville-font-family {
  font-family: var(--wp--preset--font-family--libre-baskerville) !important;
}

.has-libre-franklin-font-family {
  font-family: var(--wp--preset--font-family--libre-franklin) !important;
}

.has-literata-font-family {
  font-family: var(--wp--preset--font-family--literata) !important;
}

.has-lora-font-family {
  font-family: var(--wp--preset--font-family--lora) !important;
}

.has-merriweather-font-family {
  font-family: var(--wp--preset--font-family--merriweather) !important;
}

.has-montserrat-font-family {
  font-family: var(--wp--preset--font-family--montserrat) !important;
}

.has-newsreader-font-family {
  font-family: var(--wp--preset--font-family--newsreader) !important;
}

.has-nunito-font-family {
  font-family: var(--wp--preset--font-family--nunito) !important;
}

.has-open-sans-font-family {
  font-family: var(--wp--preset--font-family--open-sans) !important;
}

.has-overpass-font-family {
  font-family: var(--wp--preset--font-family--overpass) !important;
}

.has-petrona-font-family {
  font-family: var(--wp--preset--font-family--petrona) !important;
}

.has-piazzolla-font-family {
  font-family: var(--wp--preset--font-family--piazzolla) !important;
}

.has-playfair-display-font-family {
  font-family: var(--wp--preset--font-family--playfair-display) !important;
}

.has-plus-jakarta-sans-font-family {
  font-family: var(--wp--preset--font-family--plus-jakarta-sans) !important;
}

.has-poppins-font-family {
  font-family: var(--wp--preset--font-family--poppins) !important;
}

.has-raleway-font-family {
  font-family: var(--wp--preset--font-family--raleway) !important;
}

.has-roboto-slab-font-family {
  font-family: var(--wp--preset--font-family--roboto-slab) !important;
}

.has-roboto-font-family {
  font-family: var(--wp--preset--font-family--roboto) !important;
}

.has-rubik-font-family {
  font-family: var(--wp--preset--font-family--rubik) !important;
}

.has-sora-font-family {
  font-family: var(--wp--preset--font-family--sora) !important;
}

.has-source-sans-pro-font-family {
  font-family: var(--wp--preset--font-family--source-sans-pro) !important;
}

.has-source-serif-pro-font-family {
  font-family: var(--wp--preset--font-family--source-serif-pro) !important;
}

.has-space-mono-font-family {
  font-family: var(--wp--preset--font-family--space-mono) !important;
}

.has-texturina-font-family {
  font-family: var(--wp--preset--font-family--texturina) !important;
}

.has-work-sans-font-family {
  font-family: var(--wp--preset--font-family--work-sans) !important;
}</style>
<style id='core-block-supports-inline-css'>.wp-container-3.wp-container-3 {
  justify-content: flex-start;
}

.wp-container-4.wp-container-4 {
  gap: 0;
  justify-content: space-between;
}

.wp-container-5.wp-container-5 {
  flex-wrap: nowrap;
  gap: var(--wp--preset--spacing--40);
  justify-content: flex-start;
  align-items: flex-start;
}

.wp-container-8.wp-container-8> :where(:not(.alignleft):not(.alignright):not(.alignfull)) {
  max-width: 132px;
  margin-left: auto !important;
  margin-right: auto !important;
}

.wp-container-8.wp-container-8>.alignwide {
  max-width: 132px;
}

.wp-container-8.wp-container-8 .alignfull {
  max-width: none;
}

.wp-container-9.wp-container-9.wp-container-9.wp-container-9>*+* {
  margin-block-start: 24px;
  margin-block-end: 0;
}

.wp-duotone-unset-10>.wp-block-cover__image-background,
.wp-duotone-unset-10>.wp-block-cover__video-background {
  filter: none !important;
}

.wp-container-13.wp-container-13 {
  flex-wrap: nowrap;
}

.wp-container-6.wp-container-6>*,
.wp-container-6.wp-container-6.wp-container-6.wp-container-6>*+*,
.wp-container-9.wp-container-9>* {
  margin-block-start: 0;
  margin-block-end: 0;
}</style>
 <link crossorigin='anonymous' rel='stylesheet' id='all-css-34-1' href='https://s0.wp.com/_static/??-eJx9j8ESgjAMRH/IWHFG0IPjtxQItdo2nTSg/r3FAyLOcMu+2U026hGhoSAYRPkeouuNDUk15H1G4Owds0oLss1ko2ZRuaLPxtjXKtqnU0leDv9cswMGCRw1WiyFHwGd05bXooEkn9KttwFqzTDs19yMtSOTR/N54yvXQkIJGCOxQEfsl3otOvVSXidBHhvSgMy2za0nNq64+HNRlqfdoaqK4+0N086Tbg==?cssminify=yes' type='text/css' media='all' />
<style id='jetpack-global-styles-frontend-style-inline-css'>:root {
  --font-headings: unset;
  --font-base: unset;
  --font-headings-default: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen-Sans, Ubuntu, Cantarell, "Helvetica Neue", sans-serif;
  --font-base-default: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen-Sans, Ubuntu, Cantarell, "Helvetica Neue", sans-serif;
}</style>
<style media="print">#wpadminbar {
  display: none;
}</style>
<style media="screen">html {
  margin-top: 0px !important;
}

@media screen and (max-width: 782px) {
  html {
    margin-top: 46px !important;
  }
}</style>
<style id='wp-fonts-local'>@font-face {
  font-family: "DM Mono";
  font-style: normal;
  font-weight: 300;
  font-display: block;
  src: url('https://s0.wp.com/wp-content/themes/pub/pixl/assets/fonts/DMMono-Light.ttf') format('truetype');
  font-stretch: normal;
}

@font-face {
  font-family: "DM Mono";
  font-style: italic;
  font-weight: 300;
  font-display: block;
  src: url('https://s0.wp.com/wp-content/themes/pub/pixl/assets/fonts/DMMono-LightItalic.ttf') format('truetype');
  font-stretch: normal;
}

@font-face {
  font-family: "DM Mono";
  font-style: normal;
  font-weight: 400;
  font-display: block;
  src: url('https://s0.wp.com/wp-content/themes/pub/pixl/assets/fonts/DMMono-Regular.ttf') format('truetype');
  font-stretch: normal;
}

@font-face {
  font-family: "DM Mono";
  font-style: italic;
  font-weight: 400;
  font-display: block;
  src: url('https://s0.wp.com/wp-content/themes/pub/pixl/assets/fonts/DMMono-Italic.ttf') format('truetype');
  font-stretch: normal;
}

@font-face {
  font-family: "DM Mono";
  font-style: normal;
  font-weight: 500;
  font-display: block;
  src: url('https://s0.wp.com/wp-content/themes/pub/pixl/assets/fonts/DMMono-Medium.ttf') format('truetype');
  font-stretch: normal;
}

@font-face {
  font-family: "DM Mono";
  font-style: italic;
  font-weight: 500;
  font-display: block;
  src: url('https://s0.wp.com/wp-content/themes/pub/pixl/assets/fonts/DMMono-MediumItalic.ttf') format('truetype');
  font-stretch: normal;
}

@font-face {
  font-family: "uni 05_53";
  font-style: normal;
  font-weight: 400;
  font-display: block;
  src: url('https://s0.wp.com/wp-content/themes/pub/pixl/assets/fonts/uni05_53.ttf') format('truetype');
  font-stretch: normal;
}</style>
<style id='wp-fonts-jetpack-google-fonts'>/* latin */
@font-face {
  font-family: 'DM Mono';
  font-style: italic;
  font-weight: 300;
  font-display: fallback;
  src: url(https://fonts.wp.com/s/dmmono/v10/aFTT7PB1QTsUX8KYth-orYadb435.woff2) format('woff2');
  unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+2000-206F, U+2074, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD;
}</style>
<link rel="icon" href="roboDoc.ico" sizes="192x192" />
<link rel="apple-touch-icon" href="roboDoc.ico" />
<meta name="msapplication-TileImage" content="roboDoc.ico"/>

