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
                    v-bind:src="
                      'https://avatars0.githubusercontent.com/u/61444123?s=460&u=cbf80e36ca02b777f8be3f04e25507647f29d19b&v=4'
                    "
                    alt="Circle Image"
                    class="img-raised rounded-circle img-fluid"
                    width="200px"
                  />
                </div>
                <div class="name">
                  <h3 class="title">Christian Louboutin</h3>
                  <h6>Designer</h6>
                  <a href="#pablo" class="btn btn-just-icon btn-link btn-dribbble"><i class="fa fa-dribbble"></i></a>
                  <a href="#pablo" class="btn btn-just-icon btn-link btn-twitter"><i class="fa fa-twitter"></i></a>
                  <a href="#pablo" class="btn btn-just-icon btn-link btn-pinterest"><i class="fa fa-pinterest"></i></a>
                </div>
              </div>
            </div>
          </div>
          <div class="description text-center">
            <p>
              I’ve always been fascinated by linguistics: syntax and grammar structure/concepts have always been intellectually stimulating. When I considered these same concepts on a computing linguistics level I became drawn to the thought of studying how to write programs. From an entrepreneurial standpoint in education, I sought to study the ramifications of teaching computting linguistics simultaneously alongside reading, writing and math from the beginning of a student's educational journey at the kindergarten level continuing on to the 12th grade.
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
                  <p>Name: Chikondi</p>
                </div>
                <div class="col-md-3 mr-auto"></div>
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
export default {
  data: function() {
    return {
      message: "Personal Resume",
    };
  },
  created: function() {},
  methods: {},
};
</script>
