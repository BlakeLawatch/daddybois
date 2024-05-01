<template>
  <div class="container-fluid background-image vh-100">
    <section class="row top-page">
      <div class="col-12 col-md-6 ps-4">
        <h1 class="frijole">Catering Hours Links</h1>
        <h5>If you’re looking for treats to bring to your next function or event, look no further! Send
          us a message, let
          us know what you’re thinking, and we can work together to get you exactly what you need!</h5>
        <h1 class="candy">Catering Hours Links</h1>
        <h5>M-F 6:30am - 9:00pm</h5>
        <h5>Sat 7:00am-9:00pm</h5>
        <h5>Sun 7:00am-7:00pm</h5>
        <h1 class="penny">Catering Hours Links</h1>
        <p><a class="link" href="https://www.goldysbreakfastbistro.com/main.html">Goldys Breakfast Bistro</a></p>
        <p><a class="link" href="https://dawsontaylor.com/">Dawson Taylor</a></p>
      </div>
      <div class="col-12 col-md-5">
        <form method="post" action="https://formspree.io/f/xyyroezw">
          <div class="col-12 d-flex justify-content-between">
            <div class="col-5">
              <div class="mb-3">
                <label for="name" class="form-label">Name</label>
                <input type="text" class="form-control rounded" name="name" id="name" aria-describedby="name" required
                  minlength="5" maxlength="25">
              </div>
            </div>
            <div class="col-6">
              <div class="mb-3">
                <label for="subject" class="form-label">Subject</label>
                <select id="subject" class="w-100 py-1 rounded">
                  <option name="subject" :value="subjects" v-for="subject in subjects" :key="subject">{{ subject }}
                  </option>
                </select>
              </div>
            </div>
          </div>
          <div class="col-12">
            <!-- "form-check" was in the class on the email label line below. Made it look weird, took it out, don't know what it was for. If it doesn't work, that probably needs to go back" -->
            <div class="mb-3">
              <label for="email" class="form-label">Email address</label>
              <input type="email" class="form-control rounded" name="email" id="email" aria-describedby="emailHelp"
                required maxlength="50">
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
import { ref } from 'vue';
import Pop from '../utils/Pop';

export default {
  setup() {
    const subjects = ["Catering", "Jobs", "Art", "Other"]
    // const editable = ref({})
    return {
      subjects,
      // editable,

      // async sendEmail() {
      //   try {
      //     editable.value = {}
      //     Pop.success("Email Sent")
      //   }
      //   catch (error) {
      //     Pop.error("Email didn't send, please try again");
      //   }
      // }
    }
  }
};
</script>


<style lang="scss" scoped>
.link {
  color: black;
  font-size: 24px;
}

.link:hover {
  color: #824020;
  font-size: 26px;
  transition: ease-in-out .5s;
}
</style>