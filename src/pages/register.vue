<template>
    <q-page padding>
        <div class="q-ma-md">
            <q-card bordered>
              <q-card-section>
                    <q-input class="col-12" v-model="nome" label="Nome Completo" />
                </q-card-section>
                <!-- line -->
                <q-card-section class="row q-col-gutter-md items-start">
                    <q-input
                      class="col-4"
                      v-model="cpf"
                      mask="###.###.###-##"
                      :rules="[val => !!val || 'Field is required']"
                      label="CPF:" />
                    <q-input class="col-8" v-model="nome_mae" label="Nome da Mãe:" />
                    <span>{{ nome }}</span>
                </q-card-section>
                 <!-- line
                <q-card-section>
                    <q-input class="col-12" v-model="nome_mae" label="Nome da Mãe:" />
                </q-card-section> -->
                <!-- line -->
                <q-card-section class="row q-col-gutter-md items-start">
                    <q-input
                      class="col-6"
                      v-model="rg"
                      label="RG:"
                      :rules="[val => !!val || 'Field is required']" />
                    <q-select
                      class="col-6"
                      v-model="rg_emissor_uf"
                      :options="options"
                      label="UF-RG:" />
                    <q-input
                      class="col-6"
                      v-model="email"
                      label="Email:"
                      :rules="[val => !!val || 'Campo obrigatório']" />
                    <q-input
                      class="col-6"
                      v-model="email_confirma"
                      :options="options"
                      label="Confirmar E-mail:" />
                      <q-input
                      class="col-6"
                      v-model="senha"
                      :options="options"
                      label="Senha:" 
                      :rules="[val => !!val || 'Campo é obrigatório']" />
                    <q-input
                      class="col-6"
                      v-model="senha_confirma"
                      :options="options"
                      label="Confirmar Senha:" />
                
                </q-card-section>
                <!-- line -->
                <q-card-section>
                </q-card-section>
                <q-separtator/>
                <!-- actions -->
                <q-card-actions class="justify-center">
                    <!-- <q-space /> -->
                    <q-btn 
                    v-model="enviar" 
                    to="/#/"
                    color="white" 
                    text-color="black" 
                    label="Enviar" />
                    <!-- <q-space /> -->
                </q-card-actions>
            </q-card>
        </div>
    </q-page>
</template>
<script>
export default {
  data () {
    return {
      nome: null,
      nome_mae: null,
      rg: null,
      rg_emissor_uf: null,
      options: [
        'AC', 'AL', 'AP', 'AM', 'BA', 'CE', 'DF','ES', 'GO', 'MA', 'MT', 'MS',
         'MG', 'PA', 'PB', 'PR', 'PE', 'PI', 'RJ', 'RN','RS', 'RO', 'RR', 
         'SC', 'SP', 'SE', 'TO',  
      ],
      email: null,
      email_confirma: null,
      senha: null,
      senha_confirma: null,
      enviar: null
    }
  }
}
</script>
<style>
</style>



        <!-- <q-card
          class="login-form"
          v-bind:style="
            $q.platform.is.mobile ? { width: '80%' } : { width: '30%' }
          "
        > -->
          <!-- <q-img src="~/assets/logo.png"></q-img>
          <q-card-section>
            <q-avatar
              size="150px"
              class="absolute"
              style="top: 0; right: 25px; transform: translateY(-50%)"
            >
              <img src="~/assets/logo-pa.png" />
            </q-avatar>
            <div class="row no-wrap items-center">
              <div class="col text-h6 ellipsis">Cadastro</div>
            </div>
          </q-card-section>
          <q-card-section> -->
           


          <!-- </q-card-section> -->
