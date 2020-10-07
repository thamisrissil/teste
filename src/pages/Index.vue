<template>
  <div class ="q-pa-md" style="max-width: 400px">
    <q-form
      @reset ="onReset"
      class="q-gutter-md"
      rounded outlined label="Rounded outlined"
    >
    <div class="container">
      <q-input
        v-model="name"
        label="Digite seu nome "
    />
    <q-input
      v-model="telefone"
      label="Digite seu telefone"
    />
    <q-input
      v-model="email"
      type= "email"
      label="Digite seu email"
    />
    <q-input
      v-model="mensagem"
      type= "mensagem"
      label="Digite sua mensagem"
      lazy-rules
      :rules="[ val => val && val.lenght > 0 || 'Por favor digite sua mensagem ']"
    />
    <q-btn label="Submit" type="submit" color="grey" flat class="q-ml-sm" to="/redirecionamento"/>
    <q-btn label="resetar" type="reset" color="grey" flat class="q-ml-sm" icon="update"/>
    </div>
  </q-form>
  </div>

</template>

<script>
export default {
  name: 'PageIndex',
  methods: {
    onReset () {
      this.name = null
      this.senha = null
      this.email = null
      this.telefone = null
      this.mensagem = null
    }
  },
  data () {
    return {
      name: null,
      email: null,
      telefone: null,
      mensagem: null
    }
  }
}
</script>
<style >
  .container{
    align-items: center;
    width: 320px;
    height: 320px;
    top: 60%;
    left: 100%;
    position: relative;
    transform: translate(-50% -50%);
  }
  .q-pa-md{
     align-items: center;
     margin: 10%;
  }
  html{
     overflow-y:hidden;
     background-image:
      url("https://images.pexels.com/photos/4466492/pexels-photo-4466492.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940");
  }
  div{
    border: none;
    background-color: transparent;
  }
</style>
