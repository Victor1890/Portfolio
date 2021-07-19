<template>
  <!-- ======= About Me Section ======= -->
  <section id="about" class="about">
    <div class="container">
      <div class="section-title">
        <span>Sobre mi</span>
        <h2>Sobre mi</h2>
        <p>{{ about.aboutMe }}</p>
      </div>

      <div class="row">
        <div
          class="col-lg-4 d-flex align-items-stretch justify-content-center justify-content-lg-start"
          :style="about.photo"
        ></div>
        <div class="col-lg-8 d-flex flex-column align-items-stretch">
          <div
            class="content ps-lg-4 d-flex flex-column justify-content-center"
          >
            <div class="row">
              <div class="col-lg-6">
                <ul>
                  <li>
                    <i class="bi bi-chevron-right"></i> <strong>Nombre:</strong>
                    <span>{{ about.name }}</span>
                  </li>
                  <li>
                    <i class="bi bi-chevron-right"></i>
                    <strong>Website:</strong> <span><a :href="about.website">{{ about.website }}</a></span>
                  </li>
                  <li>
                    <i class="bi bi-chevron-right"></i> <strong>Teléfono:</strong>
                    <span>{{ about.phoneNumber }}</span>
                  </li>
                  <li>
                    <i class="bi bi-chevron-right"></i> <strong>Ciudad:</strong>
                    <span>{{ about.city }}</span>
                  </li>
                </ul>
              </div>
              <div class="col-lg-6">
                <ul>
                  <li>
                    <i class="bi bi-chevron-right"></i>
                    <strong>Título:</strong> <span>{{ about.degree }}</span>
                  </li>
                  <li>
                    <i class="bi bi-chevron-right"></i> <strong>Correo:</strong>
                    <span>{{ about.email }}</span>
                  </li>
                                 <li>
                    <i class="bi bi-chevron-right"></i> <strong>LinkedIn:</strong>
                    <span>{{ about.linkedIn }}</span>
                  </li>
                </ul>
              </div>
            </div>
            <div class="row mt-n4">
              <div class="col-md-6 mt-5 d-md-flex align-items-md-stretch">
                <div class="count-box">
                  <i class="bi bi-clock" style="color: #2cbdee"></i>
                  <span
                    data-purecounter-start="0"
                    data-purecounter-end="18"
                    data-purecounter-duration="1"
                    class="purecounter"
                  ></span>
                  <p>
                    <strong>Años de experiencia</strong> {{about.experience}}
                  </p>
                </div>
              </div>
              <div class="col-md-6 mt-5 d-md-flex align-items-md-stretch">
                <div class="count-box">
                  <i class="bi bi-award" style="color: #ffb459"></i>
                  <span
                    data-purecounter-start="0"
                    data-purecounter-end="16"
                    data-purecounter-duration="1"
                    class="purecounter"
                  ></span>
                  <p>
                    <strong>Certificaciones</strong> {{about.awards}}
                  </p>
                </div>
              </div>
            </div>
          </div>
          <!-- End .content-->

          <div class="skills-content ps-lg-4">
            <div class="progress" v-for="(skill, index) in about.skills" :key="index">
              <span class="skill"> {{skill.name}} <i class="val">{{skill.val}}%</i></span>
              <div class="progress-bar-wrap">
                <div
                  class="progress-bar"
                  role="progressbar"
                  :aria-valuenow="skill.val"
                  aria-valuemin="0"
                  aria-valuemax="100"
                ></div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <!-- End About Me Section -->
</template>

<script>
export default {
  name: "About",
  props: ['about'],
};
</script>
