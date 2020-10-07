<template>
  <div class ="q-pa-md" style="max-width: 400px">
    <q-form
      @submit ="onSubmit"
      method = "post"
      @reset ="onReset"
    >
    <div class="container">
      <q-input
        v-model="name"
        label="Digite seu nome *"
        lazy-rules
        :rules="[ val => val && val.length > 0 || 'Por favor, digite seu nome' ]"
    />
    <q-input
      v-model="telefone"
      label="Digite seu telefone"
      lazy-rules
      :rules="[ val => val && val.lenght > 0 || 'Por favor digite seu telefone ']"
    />
    <q-input
      v-model="email"
      type= "email"
      label="Digite seu email"
      lazy-rules
      :rules="[ val => val && val.lenght > 0 || 'Por favor digite seu email ']"
    />
    <q-input
      v-model="mensagem"
      type= "email"
      label="Digite sua mensagem"
      lazy-rules
      :rules="[ val => val && val.lenght > 0 || 'Por favor digite sua mensagem ']"
    />
    <q-btn label="enviar" type="submit" color="grey"/>
    </div>
  </q-form>
  </div>

</template>

<script>
export default {
  name: 'PageIndex'
}
</script>
