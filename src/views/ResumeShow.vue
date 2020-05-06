<template>
  <div class="home">
    <h1>{{ message }}</h1>

    <div class="main main-raised">
      <div class="profile-content">
        <div class="container">
          <div class="row">
            <div class="col-md-6 ml-auto mr-auto">
              <div class="profile">
                <div class="avatar">
                  <img
                    v-bind:src="photo_url"
                    alt="Circle Image"
                    class="img-raised rounded-circle img-fluid"
                    width="200px"
                  />
                </div>
                <div class="name">
                  <h3 class="title">{{ first_name }} {{ last_name }}</h3>
                  <h6>{{ email }}</h6>
                  <a v-bind:href="personal_site" class="btn btn-just-icon btn-link btn-dribbble">
                    <i class="fa fa-dribbble"></i>
                  </a>
                  <a
                    v-bind:href="`https://twitter.com/${twitter_handle}`"
                    class="btn btn-just-icon btn-link btn-twitter"
                  >
                    <i class="fa fa-twitter"></i>
                  </a>
                  <a v-bind:href="linkedin_url" class="btn btn-just-icon btn-link btn-linkedin">
                    <i class="fa fa-linkedin"></i>
                  </a>
                </div>
              </div>
            </div>
          </div>
          <div class="description text-center">
            <p>

              {{ short_bio }}

            </p>
          </div>
          <div class="row">
            <div class="col-md-6 ml-auto mr-auto">
              <div class="profile-tabs">
                <ul class="nav nav-pills nav-pills-icons justify-content-center" role="tablist">
                  <li class="nav-item">
                    <a class="nav-link active" href="#personal" role="tab" data-toggle="tab">
                      <i class="material-icons">face</i>
                      Personal
                    </a>
                  </li>
                  <li class="nav-item">
                    <a class="nav-link" href="#experiences" role="tab" data-toggle="tab">
                      <i class="material-icons">palette</i>
                      Experiences
                      
                    </a>
                  </li>
                  <li class="nav-item">
                    <a class="nav-link" href="#skills" role="tab" data-toggle="tab">
                      <i class="material-icons">done</i>

                      Skills
                    </a>
                  </li>
                  <li class="nav-item">
                    <a class="nav-link" href="#education" role="tab" data-toggle="tab">
                      <i class="material-icons">
                        school
                      </i>
                      Education
                    </a>
                  </li>
                  <li class="nav-item">
                    <a class="nav-link" href="#capstone" role="tab" data-toggle="tab">
                      <i class="material-icons">
                        folder_shared
                      </i>
                      Capstone
                    </a>
                  </li>
                </ul>
              </div>
            </div>
          </div>
          <div class="tab-content tab-space">
            <div class="tab-pane active text-center gallery" id="personal">
              <!-- Insert content related to personal section -->
              <div class="row">
                <div class="col-md-3 ml-auto">
                  
                  <p><span class="description">First Name:</span><h6>{{first_name}}</h6></p>
                   <p><span class="description">Last Name:</span><h6>{{last_name}}</h6></p>
                   <p><span class="description">Email:</span><h6>{{email}}</h6></p>
                </div>
                <div class="col-md-3 mr-auto">
                   <p><span class="description">Contact:</span><h6>{{phone}}</h6></p>
                   <p><span class="description">Github</span><h6>{{github_url}}</h6></p>
                   <p><span class="description">Twitter:</span><h6></h6>https://twitter.com/{{twitter_handle}}</p>
                </div>
              </div>
            </div>
            <!-- end of personal section -->
            <div class="tab-pane text-center gallery" id="experiences">
              <!-- Insert content related to experiences section -->
              <div class="row">
                <div class="col-md-3 ml-auto"></div>
                <div>
                  <div class="jumbotron">
                    <h1 class="display-4">Actualize Coding Bootcamp</h1>
                    <p class="lead">Apprentice</p>
                    <hr class="my-4">
                    <p>Chicago, Illinois, United States</p>
                    <p>Actualize is an intensive 18 week program focusing on full stack web development. I was challenged every day to learn and use new technologies and ideas. A lot of focus was on how to think like a developer.</p>
                    <p class="lead">
                      <a class="btn btn-primary btn-sm" href="https://anyonecanlearntocode.com/" role="button">Website</a>
                    </p>
                  </div>
                </div>
              </div>
            </div>
            <!-- end of experiences section -->
            <div class="tab-pane text-center gallery" id="skills">
              <!-- Insert content related to skills section -->
              <div class="row">
                <div class="col-md-3 ml-auto"></div>
                <ul class="list-group">
                <li class="list-group-item">Ruby</li>
                <li class="list-group-item">Ruby on Rails</li>
                <li class="list-group-item">Vue.js</li>
                <li class="list-group-item">CSS</li>
                <li class="list-group-item">Github</li>
                <li class="list-group-item">Javascript</li>
                <li class="list-group-item">HTML</li>
                <li class="list-group-item">Java</li>
              </ul>
                <div class="col-md-3 mr-auto"></div>
              </div>
            </div>
            <!-- end of skills section -->
            <div class="tab-pane text-center gallery" id="education">
              <!-- Insert content related to education section -->
              <div class="row">
                <div class="col-md-3 ml-auto"></div>
                <div class="col-md-3 mr-auto"></div>
              </div>
            </div>
            <!-- end of education section -->
            <div class="tab-pane text-center gallery" id="capstone">
              <!-- Insert content related to capstone section -->
              <div class="row">
                <div class="col-md-3 ml-auto"></div>
                <div class="col-md-3 mr-auto"></div>
              </div>
            </div>
            <!-- end of capstone section -->
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style></style>

<script>
import axios from "axios";

export default {
  data: function() {
    return {
      message: "Personal Resume",
      personalData: [],
      first_name: "Chikondi",
      last_name: "Kamvazaana",
      email: "chikondiman@gmail.com",
      phone: "2693633987",
      short_bio: "teacher gone coder",
      linkedin_url: "http://www.linkedin.com/in/chikondimore",
      twitter_handle: "chikondimore",
      personal_site: "http://www.chikondiman.com",
      online_resume_url: "",
      github_url: "http://www.github.com/chikondiman",
      photo_url:
        "https://avatars0.githubusercontent.com/u/61444123?s=460&u=cbf80e36ca02b777f8be3f04e25507647f29d19b&v=4",
    };
  },
  // created: function() {
  //   axios.get("/api/resumeapi").then( response => {
  //     console.log(response.data)
  //     this.personalData = response.data
  //   });
  // },
  methods: {},
};
</script>
