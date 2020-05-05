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
              An artist of considerable range, Chet Faker &#x2014; the name taken by Melbourne-raised, Brooklyn-based
              Nick Murphy &#x2014; writes, performs and records all of his own music, giving it a warm, intimate feel
              with a solid groove structure.
            </p>
          </div>
          <div class="row">
            <div class="col-md-6 ml-auto mr-auto">
              <div class="profile-tabs">
                <ul class="nav nav-pills nav-pills-icons justify-content-center" role="tablist">
                  <li class="nav-item">
                    <a class="nav-link active" href="#studio" role="tab" data-toggle="tab">
                      <i class="material-icons">face</i>
                      Personal
                    </a>
                  </li>
                  <li class="nav-item">
                    <a class="nav-link" href="#works" role="tab" data-toggle="tab">
                      <i class="material-icons">palette</i>
                      Experiences
                    </a>
                  </li>
                  <li class="nav-item">
                    <a class="nav-link" href="#favorite" role="tab" data-toggle="tab">
                      <i class="material-icons">done</i>

                      Skills
                    </a>
                  </li>
                  <li class="nav-item">
                    <a class="nav-link" href="#favorite" role="tab" data-toggle="tab">
                      <i class="material-icons">
                        school
                      </i>
                      Education
                    </a>
                  </li>
                  <li class="nav-item">
                    <a class="nav-link" href="#favorite" role="tab" data-toggle="tab">
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
            <div class="tab-pane active text-center gallery" id="studio">
              <div class="row">
                <div class="col-md-3 ml-auto">
                  <img v-bind:src="'./public/assets/img/examples/studio-1.jpg'" class="rounded" />
                  <img v-bind:src="'./public/assets/img/examples/studio-2.jpg'" class="rounded" />
                </div>
                <div class="col-md-3 mr-auto">
                  <img v-bind:src="'./public/assets/img/examples/studio-5.jpg'" class="rounded" />
                  <img v-bind:src="'./public/assets/img/examples/studio-4.jpg'" class="rounded" />
                </div>
              </div>
            </div>
            <div class="tab-pane text-center gallery" id="works">
              <div class="row">
                <div class="col-md-3 ml-auto">
                  <img v-bind:src="'./public/assets/img/examples/olu-eletu.jpg'" class="rounded" />
                  <img v-bind:src="'./public/assets/img/examples/clem-onojeghuo.jpg'" class="rounded" />
                  <img v-bind:src="'./public/assets/img/examples/cynthia-del-rio.jpg'" class="rounded" />
                </div>
                <div class="col-md-3 mr-auto">
                  <img v-bind:src="'./public/assets/img/examples/mariya-georgieva.jpg'" class="rounded" />
                  <img v-bind:src="'./public/assets/img/examples/clem-onojegaw.jpg'" class="rounded" />
                </div>
              </div>
            </div>
            <div class="tab-pane text-center gallery" id="favorite">
              <div class="row">
                <div class="col-md-3 ml-auto">
                  <img v-bind:src="'./assets/img/examples/mariya-georgieva.jpg'" class="rounded" />
                  <img v-bind:src="'./assets/img/examples/studio-3.jpg'" class="rounded" />
                </div>
                <div class="col-md-3 mr-auto">
                  <img v-bind:src="'./assets/img/examples/clem-onojeghuo.jpg'" class="rounded" />
                  <img v-bind:src="'./assets/img/examples/olu-eletu.jpg'" class="rounded" />
                  <img v-bind:src="'./assets/img/examples/studio-1.jpg'" class="rounded" />
                </div>
              </div>
            </div>
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
