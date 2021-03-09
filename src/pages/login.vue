<template>
  <q-layout>
    <q-page-container>
      <q-page class="flex flex-center">
        <div
          id="particles-js"
          :class="$q.dark.isActive ? 'dark_gradient' : 'normal_gradient'"
        ></div>
        <q-btn
          color="white"
          class="absolute-top-right"
          flat
          round
          @click="$q.dark.toggle()"
          :icon="$q.dark.isActive ? 'nights_stay' : 'wb_sunny'"
        />
        <q-card
          class="login-form"
          v-bind:style="
            $q.platform.is.mobile ? { width: '80%' } : { width: '30%' }
          "
        >
          <q-img src="~/assets/logo.png"></q-img>
          <q-card-section>
            <q-avatar
              size="150px"
              class="absolute"
              style="top: 0; right: 25px; transform: translateY(-57%)"
            >
              <img src="~/assets/logo-pa.png" />
            </q-avatar>
            <div class="row no-wrap items-center">
              <div class="col text-h6 ellipsis">Login</div>
            </div>
          </q-card-section>
          <q-card-section>
            <q-form class="q-gutter-md">
              <q-input 
                v-model="cpf" 
                label="CPF" 
                lazy-rules 
              />

              <q-input
                type="password"
                v-model="password"
                label="Senha"
                lazy-rules
              />

              <div class="col text-h8 ellipsis" style="margin-top: 10px">
                Ainda não tem conta? <a href="/#/register"><b>Cadastre-se</b></a>
              </div>
              <div class="col text-h8 ellipsis" style="margin-top: 10px">
                <a href="#"><b>Esqueceu sua senha?</b></a>
              </div>
              <div>
                <q-btn
                  class="center"
                  label="Entrar"
                  to="/dashboard"
                  type="button"
                  color="primary"
                  @click="loginNotify"
                />
              </div>
            </q-form>
          </q-card-section>
        </q-card>
      </q-page>
    </q-page-container>
  </q-layout>
</template>

<script type="text/javascript"></script>
<script>
export default {
  data() {
    return {
      cpf: "000.000.000-00",
      password: "admin",
    };
  },
  methods: {
    loginNotify() {
      this.$q.notify({
        message: "Login Successful",
      });
    },
  },
  mounted() {
    particlesJS("particles-js", {
      particles: {
        number: {
          value: 80,
          density: {
            enable: true,
            value_area: 800,
          },
        },
        color: {
          value: "#ffffff",
        },
        shape: {
          type: "circle",
          stroke: {
            width: 0,
            color: "#000000",
          },
          polygon: {
            nb_sides: 5,
          },
          image: {
            src: "img/github.svg",
            width: 100,
            height: 100,
          },
        },
        opacity: {
          value: 0.5,
          random: false,
          anim: {
            enable: false,
            speed: 1,
            opacity_min: 0.1,
            sync: false,
          },
        },
        size: {
          value: 3,
          random: true,
          anim: {
            enable: false,
            speed: 40,
            size_min: 0.1,
            sync: false,
          },
        },
        line_linked: {
          enable: true,
          distance: 150,
          color: "#ffffff",
          opacity: 0.4,
          width: 1,
        },
        move: {
          enable: true,
          speed: 6,
          direction: "none",
          random: false,
          straight: false,
          out_mode: "out",
          bounce: false,
          attract: {
            enable: false,
            rotateX: 600,
            rotateY: 1200,
          },
        },
      },
      interactivity: {
        detect_on: "canvas",
        events: {
          onhover: {
            enable: true,
            mode: "grab",
          },
          onclick: {
            enable: true,
            mode: "push",
          },
          resize: true,
        },
        modes: {
          grab: {
            distance: 140,
            line_linked: {
              opacity: 1,
            },
          },
          bubble: {
            distance: 400,
            size: 40,
            duration: 2,
            opacity: 8,
            speed: 3,
          },
          repulse: {
            distance: 200,
            duration: 0.4,
          },
          push: {
            particles_nb: 4,
          },
          remove: {
            particles_nb: 2,
          },
        },
      },
      retina_detect: true,
    });
  },
};
</script>

<style>
#particles-js {
  position: absolute;
  width: 100%;
  height: 100%;
  background-repeat: no-repeat;
  background-size: cover;
  background-position: 50% 50%;
}
.normal_gradient {
  background: linear-gradient(145deg, rgb(245, 246, 247) 15%, #e6e7e8 70%);
}
.dark_gradient {
  background: linear-gradient(145deg, rgb(11, 26, 61) 15%, #4c1014 70%);
}
.login-form {
  position: absolute;
}
</style>
