<template>
    <div>
        <h1>Formulario de Registro</h1>
        <Form :validation-schema="schema" @submit="onSubmit">
            <div class="form">
                <label for="nombre">Nombre:</label>
                <Field type="text" name="nombre" id="nombre" placeholder="ingrese su nombre" />
                <ErrorMessage name="nombre"></ErrorMessage>
            </div>
            <div class="form">
                <label for="correo">Correo:</label>
                <Field type="email" name="correo" id="correo" placeholder="ingrese su email" />
                <ErrorMessage name="correo"></ErrorMessage>
            </div>
            <div class="form"> 
                <button type="submit">Registrar</button>
            </div>
        </Form>
    </div>
</template>

<script setup>
    import {Form, Field, ErrorMessage } from 'vee-validate';
    import {schema} from '../schemas/validationSchema';

    const onSubmit = () => {
        console.log('Se ha enviado el formulario');
    }
</script>

<style scoped>
    .form{
        margin-bottom: 10px;
    }
</style>