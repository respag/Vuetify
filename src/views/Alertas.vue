<template>
  <div class="mt-4 ml-4">
    <div class="jumbotron">
      <h1>Componente Alert</h1>
    </div>
    <v-alert  v-model="alert" dismissible color="green darken-4"  prominent  border="left" elevation="10" colored-border
              icon="fab fa-vuejs fa-spin" class="pt-5">
              El componente <b>v-alert</b> se usa para transmitir información importante al usuario a través del uso de iconos 
        y colores de tipos contextuales. Estos tipos predeterminados vienen en 4 variaciones: 
        <b>success</b>, <b>info</b>, <b>warning</b>, y <b>error</b>. <br>
        Se asignan iconos predeterminados que ayudan a representar diferentes acciones que representa cada tipo. <br>
        Muchas partes de una alerta, como el <b>borde</b>, el <b>icono</b> y el <b>color</b>, también se pueden personalizar para 
        adaptarse a casi cualquier situación.<br>
        En nuestro ejemplo usamos:
        <ul>
          <li>
            <b>dismissible</b>: para presentar el boton<b class="text-success"> X</b> para cerrar el alert
          </li>
          <li>
            <b>color</b>: para cambiar los colores del ícono, borde y botón de cierre (en nuestro ejemplo <b>green darken-4</b>)<br>
            Para una lista de los colores permitidos vea 
            <a href="https://vuetifyjs.com/en/styles/colors#material-colors" target="_blank">material colors</a>
          </li>
          <li>
            <b>prominent</b>: Para mostrar el ícono más grande y con un halo, además de incrementar la altura del alerta.
          </li>
          <li>
            <b>border</b>: Para agregar un borde simple a uno de los lados del alerta. (En nuestro caso <b>left</b>)
          </li>
          <li>
            <b>elevation</b>: Para agregar una sombra (<b>de 1 a 24</b>) alrededor del alert. (En nuestro caso <b>10</b>)
          </li>
          <li>
            <b>colored-border</b>: Para eliminar el fondo de alerta y acentuar el borde.
          </li>
          <li>
            <b>icon</b>: Para cambiar el ícono (en nuestro caso <b>fab fa-vuejs fa-spin</b>).
            <div class="alert alert-info">
              <b>Nota</b>: Por defecto <b>Vuetify</b> usa <b>Material Design Icons</b>, pero si queremos usar <b>Font Awesome 5</b>, 
              solo tenemos que agregar en el archivo <b>index.html</b> el CDN siguiente:<br>
              <pre>&lt;link href="https://use.fontawesome.com/releases/v5.2.0/css/all.css" rel="stylesheet"></pre>
            </div>
          </li>
          <li>
            <b>class</b>: Permite agregar al alerta cualquier clase disponible. En nuestro caso como tenemos disponible 
            <b>Bootstrap.css</b> a través de su CDN, le aplicamos un padding top = 5 
          </li>
        </ul> 
     </v-alert>
     <div class="text-center">
      <v-btn v-if="!alert" color="success" @click="alert = true">
        Mostrar de nuevo el Alerta
      </v-btn>
    </div>
  </div>
</template>

<script>
export default {
  data () {
      return {
        alert: true,
      }
    },
}
</script>
