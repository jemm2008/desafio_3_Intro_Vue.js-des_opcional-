<template>
    <section id="vue-section">
        <div id="div-app" class="container">
            <div class="row">
                <div class="col-12 col-md-10 col-lg-8">
                    <div class="mt-5 d-flex flex-row justify-content-around bg-info">
                        <img :src="ruta_logo" alt="logo" width="50" class="align-self-center border border-success p-1">
                        <h2 class="my-0 py-2 text-danger me-5">{{title}}</h2>
                    </div>
                    <table class="table table-dark table-striped mt-1">
                        <thead>
                            <tr>
                                <th scope="col">#</th>
                                <th scope="col">Nombre</th>
                                <th scope="col">Apellido</th>
                                <th  class="text-center" scope="col">RUN</th>
                                <th scope="col">Fecha de Nacimiento</th>
                                <th scope="col">Edad</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr  v-for="(usr, i) in usuarios" :key="i">
                                <th scope="row">{{i+1}}</th>
                                <td>{{usr.nombre}}</td>
                                <td>{{usr.apellido}}</td>
                                <td>{{usr.RUN}}</td>
                                <td class="text-center">{{usr.fechaN}}</td>
                                <td class="text-center">{{usr.edad}}</td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
  name: 'Users_table',
  data(){
    return {
        title: "Vue.js - June - New Users Table",
        usuarios : [
                    {
                    nombre: "Jose J.",
                    apellido: "Jimenez",
                    RUN: "11.123.123-3",
                    fechaN: "03-03-1991", //fecha de nacimiento
                    edad: 30
                    },
//      
                    {
                    nombre: "Pedro",
                    apellido: "Perdomo",
                    RUN: "17.175.175-7",
                    fechaN: "11-02-2001", //fecha de nacimiento
                    edad:21
                    },
//      
                    {
                    nombre: "Diego",
                    apellido: "Diaz",
                    RUN: "23.875.875-K",
                    fechaN: "07-04-2003", //fecha de nacimiento
                    edad: 19
                    }
                    ],
        ruta_logo: "favicon.ico"
    }
  },
  props: {
    
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
</style>