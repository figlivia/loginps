<template>
    <q-page padding>
        <div class="q-ma-md">
            <q-card bordered >
             
                <!-- line -->
                <q-card-section class="row q-col-gutter-md items-start">
                      <q-input
                      class="col-6"
                      v-model="email"
                      label="Digite abaixo seu email cadastrado para recuperação:"
                      :rules="[val => !!val || 'Field is required']" />
                
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
      email: null,
      enviar: null
    }
  }
}
</script>
<style>
</style>