<template>
  <q-layout view="lHh LpR lFf">
    <q-header
      reveal
      :class="$q.dark.isActive ? 'header_dark' : 'header_normal'"
    >
      <div >
        <q-toolbar>
          <q-space/>
          <div class="divisor" />
          <h7
            >Telefone:
            <a style="color: green; margin-right: 14px"
              ><b>(91)XXXX-XXXX</b>
            </a></h7
          >
          <div class="divisor" />
          <h7
            >Ouvidoria:
            <a style="color: green; margin-right: 14px"
              ><b>ouvidoria@portal.pa.gov.br</b>
            </a></h7
          >
          <div class="divisor" />
          <h7
            >Funcionamento:
            <a style="color: green; margin-right: 14px"
              ><b>24h por dia</b>
            </a></h7
          >
          <div class="divisor" />
          <q-btn flat dense title="SIC.PA" class="q-mr-md">
            <img height="40px" src="~/assets/sicpa.png" />
          </q-btn>
          <div class="divisor" />
          <q-btn
            flat
            round
            dense
            title="Instagram"
            icon="fab fa-instagram"
            class="q-mr-md"
          />
          <div class="divisor" />
          <q-btn
            flat
            round
            dense
            title="Facebook"
            icon="facebook"
            class="q-mr-md"
            to="#"
          />
          <div class="divisor" />
          <q-btn
            flat
            round
            dense
            title="Twitter"
            icon="fab fa-twitter"
            class="q-mr-md"
            to="#"
          />
          <div class="divisor" />
          <q-space/>
        </q-toolbar>
        <div class="divisor-horizontal"/>
        <q-toolbar>

        </q-toolbar>
      </div>
    </q-header>
    <q-page-container>
      <q-page class="row no-wrap">
        <div class="col">
          <div class="full-height">
            <q-scroll-area class="col q-pr-sm full-height" visible>
              <router-view />
            </q-scroll-area>
          </div>
        </div>
      </q-page>
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  data() {
    return {
      left: false,
    };
  },
  methods: {
    logoutNotify() {
      this.$q.notify({
        message: "Logged out",
      });
    },
  },
};
</script>

<style>
.q-drawer {
  /*background-image: url(https://demos.creative-tim.com/vue-material-dashboard/img/sidebar-2.32103624.jpg) !important;*/
  background-image: url("/statics/images/lake.jpg") !important;
  background-size: cover !important;
}

.drawer_normal {
  background-color: rgba(1, 1, 1, 0.75);
}

.drawer_dark {
  background-color: #010101f2;
}

.navigation-item {
  border-radius: 5px;
}

.tab-active {
  background-color: green;
}

body {
  background: #f1f1f1 !important;
}

.header_normal {
  background: linear-gradient(
    145deg,
    rgb(32, 106, 80) 15%,
    rgb(21, 57, 102) 70%
  );
}

.header_dark {
  background: linear-gradient(145deg, rgb(0, 0, 0) 15%, rgb(220, 224, 227) 70%);
}

.divisor {
  border-left: 1px solid green;
  height: 50px;
  margin-right: 14px;
}

.divisor-horizontal {
  width: 100%;
  border-top: 1px solid green;
  margin-top: 0%;
}
</style>
