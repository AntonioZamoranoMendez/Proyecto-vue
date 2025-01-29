<template>
  <div>
    <h2>Formulario de registro</h2>
    <Form :validation-schema="schema" @submit="onSubmit">
      <div class="form">
        <label for="nombre">Nombre:</label>
        <Field name="nombre" type="text" id="nombre" placeholder="ingrese su nombre" />
        <ErrorMessage name="nombre"></ErrorMessage>
      </div>
      <div class="form">
        <label for="correo">Correo:</label>
        <Field name="email" type="email" id="correo" placeholder="ingrese su email" />
        <ErrorMessage name="email"></ErrorMessage>
      </div>
      <div class="form">
        <button type="submit">registrar</button>
      </div>
    </Form>
  </div>
</template>

<script setup>
import { Form, Field, ErrorMessage } from 'vee-validate'
import { schema } from '../schemas/validationSchema'

const onSubmit = () => {
  console.log('Se ha enviado el formulario')
}
</script>

<style scoped>
.form {
  margin-bottom: 10px;
}
</style>
