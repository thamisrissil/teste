<template>
<div class="forms">
  <q-btn outline label = Voltar to="/" icon="arrow_left" style="color: grey;" ></q-btn>
  <p>
    Nome:{{name}}
  </p>
  <p>
     Email:{{email}}
  </p>
  <p>
    Telefone:{{telefone}}
  </p>
  <p>
    Mensagem:{{mensagem}}
  </p>
  <p>
    Obrigada pelo contato! Sr(a) {{name}}
  </p>
  </div>
</template>
<script>

export default {
  name: 'SuccessPage',
  methods: {
  },
  data () {
    const formData = localStorage.getItem('formData')
    const formDataParsed = JSON.parse(formData)
    return {
      name: formDataParsed.name,
      email: formDataParsed.email,
      telefone: formDataParsed.telefone,
      mensagem: formDataParsed.mensagem
    }
  }
}
</script>
<style>
  p {
    text-align: center;
    font-size: 20px;
    line-height: 1.5;
    text-decoration: underline;
    text-transform: uppercase;
  }
   html{
     overflow-y:hidden;
     background-image:
      url("https://images.pexels.com/photos/4466492/pexels-photo-4466492.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940");
  }
</style>
