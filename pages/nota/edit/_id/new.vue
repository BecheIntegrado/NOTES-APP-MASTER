<template>
    <div class="card bg-warning my-5"> 
        <div class="card-body">
            <b-form @submit.prevent="save"> 
                <b-form-group>
                    <b-form-input
                        class="bg-warni"
                        v-model="email"
                        type="email"
                        placeholder="E-mail"
                        required
                    ></b-form-input>
                </b-form-group>
            </b-form>
        </div>


        <b-button type="button" variant="warnig">
            
            <b-icon icon="check2-square"></b-icon>
            
        </b-button>

        <b-button type="button">
            
            <b-icon type="button" variant="dark" ></b-icon>

        </b-button>

    </div>
</template>

<script>
    export default {
        layout:"home",
        data (){
            return {
                nota:{
                    titulo: null,
                    descricao:null,
                    checklist:[],
                    tag:[]
                }
            }
        },
        methods: {
            async adiconar(){
                this.$store.dspatch('nota/add', this.nota)
            }
        }
    }
    Vue.component('button-counter', {
        data: function () {
        return {
        count: 0
        }
     },
  template: '<button v-on:click="count++">Você clicou em mim {{ count }} vezes.</button>'
})
    
</script>

<style>
</style>
