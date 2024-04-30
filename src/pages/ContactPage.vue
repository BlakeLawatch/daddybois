<template>
  <div class="container-fluid background-image vh-100">
    <section class="row top-page">
      <div class="col-12 col-md-7">

      </div>
      <div class="col-12 col-md-5">
        <form>
          <div class="col-12 d-flex justify-content-between">
            <div class="col-5">
              <div class="mb-3">
                <label for="name" class="form-label">Name</label>
                <input type="text" class="form-control" id="name" aria-describedby="emailHelp" required minlength="5"
                  maxlength="25">
              </div>
            </div>
            <div class="col-5">
              <div class="mb-3">
                <label for="subject" class="form-label">Subject</label>
                <select name="subject" id="subject" class="w-100 py-1">
                  <option :value="subjects" v-for="subject in subjects" :key="subject">{{ subject }}</option>
                </select>
              </div>
            </div>
          </div>
          <div class="mb-3 form-check">
            <label for="email" class="form-label">Email address</label>
            <input type="email" class="form-control" id="email" aria-describedby="emailHelp" required maxlength="50">
          </div>
          <div class="mb-3">
            <label for="description" class="form-label">Description</label>
            <textarea name="description" id="description" cols="80" rows="5" required minlength="10"
              maxlength="200"></textarea>
          </div>
          <button type="submit" class="btn btn-danger text-end">Submit</button>
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
    const subjects = ["Catering", "Jobs", "Art", "Other"]
    return {
      subjects
    }
  }
};
</script>


<style lang="scss" scoped></style>