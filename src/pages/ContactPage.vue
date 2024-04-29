<template>
  <div class="container-fluid background-image vh-100">
    <section class="row top-page">
      <div class="col-12 col-md-7">

      </div>
      <div class="col-12 col-md-5">
        <form>
          <div class="mb-3">
            <label for="name" class="form-label">Name</label>
            <input type="text" class="form-control" id="name" aria-describedby="emailHelp">
          </div>
          <div class="mb-3">
            <label for="subject" class="form-label">Subject</label>
            <input type="text" class="form-control" id="subject">
          </div>
          <div class="mb-3 form-check">
            <label for="exampleInputEmail1" class="form-label">Email address</label>
            <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp">
            <div id="emailHelp" class="form-text">We'll never share your email with anyone else.</div>
          </div>
          <div class="mb-3">
            <label for="Description" class="form-label">Description</label>
            <input type="text" class="form-control" id="Description">
          </div>
          <button type="submit" class="btn btn-primary">Submit</button>
        </form>
      </div>
    </section>

  </div>
</template>


<script>
import { AppState } from '../AppState';
import { computed, reactive, onMounted } from 'vue';
export default {
  setup() {
    return {}
  }
};
</script>


<style lang="scss" scoped></style>