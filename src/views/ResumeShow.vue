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
                  <h3 class="title">{{ student.first_name }} {{ student.last_name }}</h3>
                  <h6>{{ student.email }}</h6>
                  <a v-bind:href="student.personal_site_url" class="btn btn-just-icon btn-link btn-dribbble">
                    <i class="fa fa-dribbble"></i>
                  </a>
                  <a
                    v-bind:href="student.twitter_handle"
                    class="btn btn-just-icon btn-link btn-twitter"
                  >
                    <i class="fa fa-twitter"></i>
                  </a>
                  <a v-bind:href="student.linkedin_url" class="btn btn-just-icon btn-link btn-linkedin">
                    <i class="fa fa-linkedin"></i>
                  </a>
                </div>
              </div>
            </div>
          </div>
          <div class="description text-center">
            <p>

              {{ student.short_bio }}

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
                  
                  <p><span class="description">First Name:</span><h6>{{student.first_name}}</h6></p>
                   <p><span class="description">Last Name:</span><h6>{{student.last_name}}</h6></p>
                   <p><span class="description">Email:</span><h6>{{student.email}}</h6></p>
                </div>
                <div class="col-md-3 mr-auto">
                   <p><span class="description">Contact:</span><h6>{{student.phone_number}}</h6></p>
                   <p><span class="description">Github</span><h6>{{student.github_url}}</h6></p>
                   <p><span class="description">Twitter:</span><h6></h6>{{student.twitter_handle}}</p>
                </div>
              </div>
            </div>
            <!-- end of personal section -->
            <div class="tab-pane text-center gallery" id="experiences">
              <!-- Insert content related to experiences section -->
              
               
                <div v-bind:key="experience.id" v-for="experience in student.experiences">>
                  <div class="jumbotron">
                    <h1 class="display-4">{{experience.company}}</h1>
                    <p class="lead">{{experience.job_title}}</p>
                    <hr class="my-4">
                    
                    <p>{{experience.details}}</p>
                    <p class="lead">{{experience.start_date}} to {{experience.end_date}} </p>
                    <p class="lead">
                      <a class="btn btn-primary btn-sm" href="https://anyonecanlearntocode.com/" role="button">Website</a>
                    </p>
                  </div>
                </div>
              
            </div>
            <!-- end of experiences section -->
            <div class="tab-pane text-center gallery" id="skills">
              <!-- Insert content related to skills section -->
              <div v-bind:key="skill.id" v-for="skill in student.skills">
             
                <ul class="list-group">
                <li class="list-group-item">{{skill.name}}</li>
                              </ul>
                
              </div>
            </div>
            
            <!-- end of skills section -->
            
            <div class="tab-pane text-center gallery" id="education"  >
              <div v-bind:key="education.id" v-for="education in student.education">
              <!-- Insert content related to education section -->
                  <div class="jumbotron jumbotron-fluid">
                  <div class="container">
                    <h1 class="display-6">{{education.university}}</h1>
                    <p class="lead">{{education.degree}}</p>
                    <p class="lead">{{education.details}}</p>
                    <p class="lead">{{education.start_date}} to {{education.end_date}} </p>
                  </div>
            </div>
                                          
            </div>
            </div>
            <!-- end of education section -->
            <div class="tab-pane text-center gallery" id="capstone">
              <!-- Insert content related to capstone section -->
              <div v-bind:key="capstone.id" v-for="capstone in student.capstones">
                <div class="jumbotron">
                  <h1 class="display-4">{{student.capstone}}</h1>
                  <p class="lead">{{capstone.name}}</p>
                  <hr class="my-4">
                  <p>{{capstone.description}}</p>
                  <p class="lead">
                    <a class="btn btn-primary btn-sm" v-bind:href="capstone.screenshot_url" role="button">Check it on Github</a>
                  </p>
                </div>
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
      student: [],
      first_name: "Chikondi",
      last_name: "Kamvazaana",
      email: "chikondiman@gmail.com",
      phone_number: "2693633987",
      short_bio: "teacher gone coder",
      linkedin_url: "http://www.linkedin.com/in/chikondimore",
      twitter_handle: "chikondimore",
      personal_site_url: "http://www.chikondiman.com",
      online_resume_url: "",
      github_url: "http://www.github.com/chikondiman",
      photo_url:
        "https://avatars0.githubusercontent.com/u/61444123?s=460&u=cbf80e36ca02b777f8be3f04e25507647f29d19b&v=4",
      educations: [{
        institution: "Andrews University",
        description: "Bachelor of Arts(BA), Secondary Education of Teaching",
        start_date: "2009",
        end_date: "2014"
      },
      {
        institution: "Andrews University",
        description: "Bachelor of Arts(BA), Secondary Education of Teaching",
        start_date: "2009",
        end_date: "2014"
      }
      ]
    };
  },
  created: function() {
    axios.get("/api/students/2").then( response => {
      console.log(response.data)
      this.student = response.data;
    });
  },
  methods: {},
};
     
</script>


