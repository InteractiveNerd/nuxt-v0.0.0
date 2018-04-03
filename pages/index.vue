<template>
  <div class="container-fluid">
    <!-- Hero Section -->
    <section class="row align-items-center">
      <!-- create container here that can move hide all items > then show the thankyou form -->
      <div class="col">
        <div class="row">
          <div class="col text-center p-3">So far {{ signUpCount }} have signed up!</div>
        </div>
        <div class="row">
          <div class="col text-center p-3"><img src="http://via.placeholder.com/350x100" alt="animation truck"></div>
        </div>
      </div>

      <div class="col">
        <!-- @ on submit . preventDefault -->
        <form class="form-signin needs-validation" @submit.prevent="signMeUp" v-if="show">
          <div class="text-center mb-4">
            <h1 class="moveMe h3 mb-3 font-weight-normal">Hello {{ form.name }}, help us add the Truck Emoji</h1>
          </div>

          <div class="row">

            <div class="col">
              <div class="form-label-group">
                <input type="text" id="inputName" class="form-control" placeholder="Name" v-model="form.name" required autofocus>
                <label for="inputName">NAME</label>
              </div>
            </div>

            <div class="col">
              <div class="form-label-group">
                <input type="email" id="inputEmail" class="form-control" placeholder="Email address" v-model="form.email" required autofocus>
                <label for="inputEmail">EMAIL</label>
              </div>
            </div>

          </div>

          <div class="form-label-group">
            <select class="custom-select d-block w-100 form-control" id="inputState" v-model="form.country" required autofocus>
              <option value="">COUNTRY</option>
              <option>California</option>
            </select>
          </div>

          <div class="checkbox mb-3">
            <label>
              <input type="checkbox" value="remember-me" v-model="form.checked" required> GDPR Compliance
            </label>
          </div>
          <button class="btn btn-lg btn-primary btn-block" type="submit">Sign me up!</button>
          <p v-if="errors">{{ errors }}</p>
          <p v-else>No Errors</p>
        </form>
      </div>
    </section>
    <!-- Section 2 -->
    <section class="row align-items-center">
      <div class="col-12 text-center p-3">
        <img src="http://via.placeholder.com/500x200" class="img-fluid" alt="FPO Image">
      </div>
      <div class="col-12 text-center p-3">
        <p>Leave me alone. Hey, McFly, I thought I told you never to come in here.</p>
      </div>
    </section>
    <!-- Section 3 -->
    <section class="row align-items-center">
      <div class="col-3"></div>
      <div class="col-6 text-center p-3">
        <p></p>
        <p>Leave me alone. Hey, McFly, I thought I told you never to come in here. Well it's gonna cost you. How much money you got on you? Marty, that's completely out of the question, you must not leave this house. you must not see anybody or talk to anybody. Anything you do could have serious reprocautions on future events. Do you understand?</p>
      </div>
      <div class="col-3"></div>
      <div class="col-12 text-center p-3">
        <img src="http://via.placeholder.com/100x50" class="img-fluid" alt="FPO Image">
      </div>
    </section>
    <!-- Section 4 -->
    <section class="row align-items-center">
      <div class="col-1"></div>
      
      <div class="col text-center">
        <div class="row">
          <div class="col"><img src="http://via.placeholder.com/250x250" class="img-fluid img-thumbnail" alt="FPO Image"></div>
          <div class="w-100"></div>
          <div class="col p-3">Caption Here</div>
        </div>
      </div>
      <div class="col text-center">
        <div class="row">
          <div class="col"><img src="http://via.placeholder.com/250x250" class="img-fluid img-thumbnail" alt="FPO Image"></div>
          <div class="w-100"></div>
          <div class="col p-3">Caption Here</div>
        </div>
      </div>
      <div class="col text-center">
        <div class="row">
          <div class="col"><img src="http://via.placeholder.com/250x250" class="img-fluid img-thumbnail" alt="FPO Image"></div>
          <div class="w-100"></div>
          <div class="col p-3">Caption Here</div>
        </div>
      </div>
      <div class="col-1"></div>
    </section>
    <!-- Section 5 -->
    <section class="row align-items-center">
      <div class="col text-center">
        <div class="row align-items-center">
          <div class="col p-3"><img src="http://via.placeholder.com/150x100" class="img-fluid" alt="FPO Image"></div>
        </div>
        <div class="row align-items-center">
          <div class="col"><img class="rounded-circle img-fluid" src="http://via.placeholder.com/150x150" alt="FPO Image"></div>
          <div class="col">
            <p class="pt-3 display-4">SPREAD THE WORD!</p>
            <div class="line p-3">________________</div>
            <p class="p-3">You must not see anybody or talk to anybody. Anything you do could have serious reprocautions on future events.</p>
          </div>
          <div class="col"><img class="rounded-circle img-fluid" src="http://via.placeholder.com/150x150" alt="FPO Image"></div>
        </div>
      </div>
    </section>
    <!-- Section 6 -->
    <section class="row align-items-center">
      <div class="col text-center">
        <div class="row p-5">
          <div class="col"><img src="http://via.placeholder.com/100x100" class="img-fluid" alt="FPO Image"></div>
        </div>
        <div class="row p-3">
          <div class="col"></div>
          <div class="col-4"><p class="display-4">HOW DO WE GET THERE?</p></div>
          <div class="col"></div>
        </div>
        <div class="row p-3">
          <div class="col">
            <img src="http://via.placeholder.com/900x250" class="img-fluid" alt="FPO Image">
          </div>
        </div>
      </div>
    </section>
    <footer class="row align-items-center p-3">
      <div class="col-10">
        <p>Leave me alone. Hey, McFly, I thought I told you never to come in here. Well it's gonna cost you. How much money you got on you? Marty, that's completely out of the question, you must not leave this house. you must not see anybody or talk to anybody. Anything you do could have serious reprocautions on future events. Do you understand?</p>
      </div>
      <div class="col-2"><img src="http://via.placeholder.com/100x50" class="img-fluid" alt="FPO Image"></div>
    </footer>
  </div>
</template>

<script>
import gsap from 'gsap'
import axios from 'axios'
import { ScrollContainer, ScrollItem } from 'vue-scrollmonitor'

export default {
  props: [
  ],
  name: 'Ford',
  components: {
    ScrollContainer,
    ScrollItem,
  },
  data() {
    return {
      /** @prop {obj} - Form input Values. */
      form: {
        name: '',
        email: '',
        country: null,
        checked: []
      },
      countrys: [
        { text: 'Select Country', value: null },
        'America', 'Europe', 'Canada', 'Austrailia'
      ],
      show: true,
      signUpCount: '3,400',
      signUpFormId: '',
      signUpFormUrl: `http://jsonplaceholder.typicode.com/posts`, // ${signUpFormId}
      posts: [],
      errors: null,
    };
  },
  created() {
    // axios.get(`http://jsonplaceholder.typicode.com/posts`) //replace when you get proper URL
    // .then(response => {
    //   // JSON responses are automatically parsed.
    //   this.posts = response.data
    // })
    // .catch(e => {
    //   this.errors.push(e)
    // })
    // async / await version (created() becomes async created())
    //
    // try {
    //   const response = await axios.get(`http://jsonplaceholder.typicode.com/posts`)
    //   this.posts = response.data
    // } catch (e) {
    //   this.errors.push(e)
    // }
  },
  mounted: function () {
    // On page load get total number of submissions
    // jQuery.get("/utils/cons_counter/signup_counter.ajax.php?signup_form_id="+signup_form_id, load_counter);
    // forms = document.getElementsByClassName('needs-validation');
    // simple tweenmax test
    // TweenMax.to('.form-signin', 1, {y: -150, ease:Power2.easeOut});
    // Loop over them and prevent submission
    // this.validation = Array.prototype.filter.call(forms, function(form) {
    //   form.addEventListener('submit', function(event) {
    //     if (form.checkValidity() === false) {
    //       event.preventDefault();
    //       event.stopPropagation();
    //     }
    //     form.classList.add('was-validated');
    //   }, false);
    // });
  },
  methods: {
    signMeUp (evt) {
      console.log('submit fired');
      // evt.preventDefault();
      // alert(JSON.stringify(this.form));
    },
    onReset (evt) {
      evt.preventDefault();
      /* Reset our form values */
      this.form.email = '';
      this.form.name = '';
      this.form.country = null;
      this.form.checked = [];
      /* Trick to reset/clear native browser form validation state */
      this.show = false;
      this.$nextTick(() => { this.show = true });
    },
    countSignups: function (signup_form_id) {
      
    },
    load_counter: function (data) {
      this.signUpCount;
    }
  }
}

// function count_signups(signup_form_id){
 
//   // This function formats numbers by adding commas
//   function numberFormat(nStr){
//     nStr += '';
//     x = nStr.split('.');
//     x1 = x[0];
//     x2 = x.length > 1 ? '.' + x[1] : '';
//     var rgx = /(\d+)(\d{3})/;
//     while (rgx.test(x1))
//       x1 = x1.replace(rgx, '$1' + ',' + '$2');
//     return x1 + x2;
//   }
//   function load_counter(data){
//     document.getElementById('signup_counter').innerHTML = numberFormat(data);
//   }
//   jQuery.get("/utils/cons_counter/signup_counter.ajax.php?signup_form_id="+signup_form_id, load_counter);
// }
</script>

<style lang='scss'>
@import '../node_modules/bootstrap/dist/css/bootstrap.css';

/*make each section it's own SCSS*/
:root {
  --input-padding-x: .75rem;
  --input-padding-y: .75rem;
}

html,
body {
  height: 100%;
}

body {
  
}
/* Dev helpers/area */
section {
  border: 1px solid #007bff;
}

/* working area */
section {
  min-height: 700px;
}
footer {
  background: black;
  color: white;
  font-size: 10px;
}

.form-signin {
  width: 100%;
  max-width: 420px;
  padding: 15px;
  margin: 0 auto;
}

.form-label-group {
  position: relative;
  margin-bottom: 1rem;
}

.form-label-group > input,
.form-label-group > label {
  padding: var(--input-padding-y) var(--input-padding-x);
}

.form-label-group > label {
  position: absolute;
  top: 0;
  left: 0;
  display: block;
  width: 100%;
  margin-bottom: 0; /* Override default `<label>` margin */
  line-height: 1.5;
  color: #495057;
  border: 1px solid transparent;
  border-radius: .25rem;
  transition: all .1s ease-in-out;
}

.form-label-group input::-webkit-input-placeholder {
  color: transparent;
}

.form-label-group input:-ms-input-placeholder {
  color: transparent;
}

.form-label-group input::-ms-input-placeholder {
  color: transparent;
}

.form-label-group input::-moz-placeholder {
  color: transparent;
}

.form-label-group input::placeholder {
  color: transparent;
}

.form-label-group input:not(:placeholder-shown) {
  padding-top: calc(var(--input-padding-y) + var(--input-padding-y) * (2 / 3));
  padding-bottom: calc(var(--input-padding-y) / 3);
}

.form-label-group input:not(:placeholder-shown) ~ label {
  padding-top: calc(var(--input-padding-y) / 3);
  padding-bottom: calc(var(--input-padding-y) / 3);
  font-size: 12px;
  color: #777;
}
</style>
