<template>
  <Navbar />
  <div class="container-fluid background-image">
    <section class="row top-page">
      <div class="col-11 col-md-6 ps-4 mb-3">
        <p class="arima fs-1 fw-bold">Catering</p>
        <h5>If you’re looking for treats to bring to your next function or event, look no further! Send
          us a message, let us know what you’re thinking, and we can work together to get you exactly what you need!
        </h5>
        <p class="arima fs-1 fw-bold">Hours</p>
        <h5>M-F 6:30am - 9:00pm</h5>
        <h5>Sat 7:00am-9:00pm</h5>
        <h5>Sun 7:00am-7:00pm</h5>
        <p class="arima fs-1 fw-bold">Links</p>
        <div class="link-group">
          <a target="_blank" class="link me-5" href="https://www.goldysbreakfastbistro.com/main.html">Goldys
            Breakfast
            Bistro</a>
          <a target="_blank" class="link me-5" href="https://dawsontaylor.com/">Dawson Taylor</a>
          <a target="_blank" class="link" href="https://stagecoachidaho.com/">Stagecoach Inn</a>
        </div>
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
          <button type="submit" class="btn btn-danger text-end mb-2">Submit</button>
        </form>
      </div>
    </section>
    <section class="map row">
      <div class="col-md-12">
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2888.6032483017666!2d-116.20486968824567!3d43.61480187098345!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x54aef8e4c7e7821b%3A0xaddfc950248b7a8e!2sGoldy&#39;s%20Corner!5e0!3m2!1sen!2sus!4v1717523772689!5m2!1sen!2sus"
          width="1500" height="450" style="border:0;" loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"></iframe>
      </div>
    </section>

  </div>
  <Bottom />
</template>


<script>
import { ref } from 'vue';
import Pop from '../utils/Pop';
import Navbar from '../components/Navbar.vue';

export default {
  setup() {
    const subjects = ["Catering", "Jobs", "Art", "Other"]

    return {
      subjects,

    }
  }
};
</script>


<style lang="scss" scoped>
.link {
  color: black;
  font-size: 1.5rem;
}

.link:hover {
  color: #824020;
  text-shadow: 1px 1px 3px #824020;
  transition: ease-in-out .3s;
}


p {
  margin-bottom: 0;
  padding-top: .5rem;
}

.link-group {
  display: flex;
}

@media (max-width: 767px) {
  .link-group {
    display: grid;
  }
}

textarea {
  max-width: 100%;
}


form:valid button[type="submit"] {


  animation: pulse 1s infinite;


  // background-color: #C9A243;
  @keyframes pulse {
    0% {
      box-shadow: 0 0 0 0 var(--bs-success), 0 0 0 0 var(--bs-success);
    }

    40% {
      box-shadow: 0 0 0 0 var(--bs-success), 0 0 0 3px var(--bs-success);
    }

    80% {
      box-shadow: 0 0 0 0 var(--bs-success), 0 0 0 7px rgba(255, 4, 0, 0);
    }

    100% {
      box-shadow: 0 0 0 0 var(--bs-success), 0 0 0 3px rgba(255, 4, 0, 0);
    }
  }


}

@media (max-width: 767px) {
  .map {
    visibility: hidden;
  }
}

// button {
//   animation: pulse 1s infinite;
// }

// button.log[data-state="valid"] {

//   // background-color: #C9A243;
//   @keyframes pulse {
//     0% {
//       box-shadow: 0 0 0 0 var(--bs-success), 0 0 0 0 var(--bs-success);
//     }

//     40% {
//       box-shadow: 0 0 0 0 var(--bs-success), 0 0 0 3px var(--bs-success);
//     }

//     80% {
//       box-shadow: 0 0 0 0 var(--bs-success), 0 0 0 7px rgba(255, 4, 0, 0);
//     }

//     100% {
//       box-shadow: 0 0 0 0 var(--bs-success), 0 0 0 3px rgba(255, 4, 0, 0);
//     }
//   }
// }


// @keyframes pulse {
//   0% {
//     transform: scale(1);
//   }

//   50% {
//     transform: scale(1.05);
//   }

//   100% {
//     transform: scale(1);
//   }
// }</style>