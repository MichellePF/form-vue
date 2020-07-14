<template>
    <form action="" class="form-register">
        <h4>Formulario Dojo</h4>
        <input class="controls" type="text" name="nombres" id="nombres" placeholder="Ingrese su nombre" v-model="nombre">
        <input class="controls" type="email" name="email" id="email" placeholder="Ingrese su correo" v-model="email">
        <select class="controls" v-model="selected">
            <option disabled value="">Selecciona tu ubicación</option>
            <option>Chile</option>
            <option>México</option>
            <option>Argentina</option>
            <option>Colombia</option>
            <option>España</option>
            <option>Estados Unidos</option>
        </select>
        <select class="controls" v-model="selected">
            <option disabled value="">Selecciona tu lenguaje favorito</option>
            <option>JavaScript</option>
            <option>Java</option>
            <option>Dart</option>
            <option>Python</option>
            <option>C#</option>
            <option>PHP</option>
        </select>
        <textarea class="controls" v-model="message" placeholder="Comentarios"></textarea>
        <p>Estoy de acuerdo con <a href="#">Términos y Condiciones</a></p>
        <input class="botons" type="submit" value="Registrar" v-model="enviar">
        <p><a href="#">¿Ya tengo Cuenta?</a></p>
    </form>
</template>

<script>
    export default {
        name: "FormDojo",
        data: function(){
            return {
                nombre: '',
                email: '',
                selected: '',
                message: '',
                enviar: 'Enviar'
            }
        }
    }
</script>

<style scoped>
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }


    .form-register {
        width: 400px;
        background: #24303c;
        padding: 30px;
        margin: auto;
        margin-top: 100px;
        border-radius: 4px;
        font-family: 'calibri';
        color: white;
        box-shadow: 7px 13px 37px #000;
    }

    .form-register h4 {
        font-size: 22px;
        margin-bottom: 20px;
    }

    .controls {
        width: 100%;
        background: #24303c;
        padding: 10px;
        border-radius: 4px;
        margin-bottom: 16px;
        border: 1px solid #1f53c5;
        font-family: 'calibri';
        font-size: 18px;
        color: white;
    }

    .form-register p {
        height: 40px;
        text-align: center;
        font-size: 18px;
        line-height: 40px;
    }

    .form-register a {
         color: white;
        text-decoration: none;
    }

    .form-register a:hover {
        color: white;
        text-decoration: underline;
    }

    .form-register .botons {
        width: 100%;
        background: #1f53c5;
        border: none;
        padding: 12px;
        color: white;
        margin: 16px 0;
        font-size: 16px;
    }

    .form-register .botons:hover {
        background: green;
        border: 1px solid white;
    } 

</style>