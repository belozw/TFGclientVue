<template>
  <div id="app">
    <el-container>
      <el-aside width="250px">
        <div class="logo-container">
          <img src="../src/assets/calma_logov2.png" class="image">
        </div>
            <el-menu
              default-active="2"
              class="el-menu-vertical-demo"
              @open="handleOpen"
              @close="handleClose"
              background-color="#545c64"
              text-color="#fff"
              active-text-color="#5DBCD2">

          <el-menu-item index="1">
            <i class="el-icon-info"></i>
            <span>Inicio</span>
          </el-menu-item>

          <el-menu-item index="2">
            <i class="el-icon-edit"></i>
            <span>Enviar telecomandos</span>
          </el-menu-item>

          <el-menu-item index="3">
            <i class="el-icon-view"></i>
            <span>Visualizar datos</span>
          </el-menu-item>

          <el-menu-item index="4">
            <i class="el-icon-setting"></i>
            <span>Ajustes</span>
          </el-menu-item>
        </el-menu>
      </el-aside>
      <el-container>
        <el-header style="height: 114px">
          <el-alert
            title="Construyendo el sitio."
            type="error"
            description="Aún en estado de desarrollo, vuelva mas tarde porfavor."
            :closable="false"
            show-icon>
          </el-alert>
        </el-header>
        <el-main>
          <el-switch
            v-model="value3"
            active-text="Deshabilitar comandos"
            inactive-text="Habilitar comandos">
          </el-switch>
        </el-main>
      </el-container>
    </el-container>
  </div>
</template>

<script>
export default {
  name: 'app',
  data: function() {
      return {
        value3: false
      };
    }
  };
</script>

<style>
#app {
  font-family: Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

.el-aside {
  background: #545c64;
  color: white;
  min-height: 100vh; /**altura maxima**/
}
.el-menu {
  border-right: 0 !important; /**esto es para quitar un borde pequeño que se forma al poner el menu**/
}
.el-header {
  background: #434A50;
}
.el-main {
  background: #363c42;
}
.el-alert {
  margin-top: 30px;
}

.logo-container {
  padding: 15px; /**espaciado logo**/
  background: #434A50;
}
.container {
  max-width: auto; /** cambiar esto por 1200px si algo NO FUNCIONA*/
  margin: 0px;
}

body {
  margin: 0; /**para quitar los bordes molestos por defecto**/
}
</style>
