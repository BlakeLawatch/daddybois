<template>
  <div class="container-fluid background-image vh-100">
    <section class="row top-page">
      <div class="col-12 col-md-7">

      </div>
      <div class="col-12 col-md-5">
        <form method="post">
          <div class="col-12 d-flex justify-content-between">
            <div class="col-5">
              <div class="mb-3">
                <label for="name" class="form-label">Name</label>
                <input type="text" class="form-control rounded" id="name" aria-describedby="emailHelp" required
                  minlength="5" maxlength="25">
              </div>
            </div>
            <div class="col-6">
              <div class="mb-3">
                <label for="subject" class="form-label">Subject</label>
                <select name="subject" id="subject" class="w-100 py-1 rounded">
                  <option :value="subjects" v-for="subject in subjects" :key="subject">{{ subject }}</option>
                </select>
              </div>
            </div>
          </div>
          <div class="col-12">
            <!-- "form-check" was in the class on the email label line below. Made it look weird, took it out, don't know what it was for. If it doesn't work, that probably needs to go back" -->
            <div class="mb-3">
              <label for="email" class="form-label">Email address</label>
              <input type="email" class="form-control rounded" id="email" aria-describedby="emailHelp" required
                maxlength="50">
            </div>
            <div class="mb-3">
              <label for="description" class="form-label">Description</label>
              <textarea name="description" id="description" cols="80" rows="5" required minlength="10"
                maxlength="200"></textarea>
            </div>

          </div>
          <button type="submit" class="btn btn-danger text-end">Submit</button>
        </form>
      </div>
    </section>

  </div>
</template>


<script>
import { AppState } from '../AppState';
import { computed, reactive, onMounted, ref } from 'vue';
import Pop from '../utils/Pop';
export default {
  setup() {
    const subjects = ["Catering", "Jobs", "Art", "Other"]
    const editable = ref({})
    return {
      subjects,

      async sendEmail() {
        try {
          editable.value = {}
          Pop.success("Email Sent")
        }
        catch (error) {
          Pop.error("Email didn't send, please try again");
        }
      }
    }
  }
};
</script>


<style lang="scss" scoped></style>