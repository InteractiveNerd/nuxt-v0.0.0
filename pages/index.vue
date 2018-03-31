<template>
  <div class="container-fluid">
    <!-- Hero Section -->
    <section class="row align-items-center">
      <!-- create container here that can move hide all items > then show the thankyou form -->
      <div class="col">
        <div class="row">
          <div class="col text-center p-3"><img src="http://via.placeholder.com/250x100" alt="text here"></div>
        </div>
        <div class="row">
          <div class="col text-center p-3"><img src="http://via.placeholder.com/350x100" alt="animation truck"></div>
        </div>
      </div>

      <div class="col">
        <form class="form-signin">
          <div class="text-center mb-4">
            <h1 class="moveMe h3 mb-3 font-weight-normal">Short compelling headline goes here</h1>
          </div>

          <div class="row">

            <div class="col">
              <div class="form-label-group">
                <input type="text" id="inputName" class="form-control" placeholder="Name" required autofocus>
                <label for="inputName">NAME</label>
              </div>
            </div>

            <div class="col">
              <div class="form-label-group">
                <input type="email" id="inputEmail" class="form-control" placeholder="Email address" required autofocus>
                <label for="inputEmail">EMAIL</label>
              </div>
            </div>

          </div>

          <div class="form-label-group">
            <select class="custom-select d-block w-100 form-control" id="inputState" required autofocus>
              <option value="">COUNTRY</option>
              <option>California</option>
            </select>
          </div>

          <div class="checkbox mb-3">
            <label>
              <input type="checkbox" value="remember-me"> Remember me
            </label>
          </div>
          <button class="btn btn-lg btn-primary btn-block" type="submit">Sign me up!</button>
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
import AppLogo from '~/components/AppLogo.vue'

export default {
  components: {
    AppLogo
  }
}
</script>

<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
