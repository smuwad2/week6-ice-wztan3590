<script>
    export default { 
        data() {
            return {
                id: "demo1",
                blueBoth: true
            }
        },
        methods: { 
   			changeColor() {
                this.blueBoth = !this.blueBoth

                // if(this.blueBoth != true) {
                //     this.blueBoth = true
                // } else {
                //     this.blueBoth = false
                // }
            }
		}
    }
</script>

<template>
    
    <!-- Modify code here -->
    <div class="container">
        <div v-bind:id="id" class="m-2" v-bind:class="{'blueBox' : blueBoth, 'redBox' : !blueBoth}">
            div ID : {{id}} 
        </div>
        
        <!-- btn-danger & btn-primary -->
        <button type="button" v-bind:class="{'btn btn-primary' : blueBoth, 'btn btn-danger' : !blueBoth}" 
        @click="changeColor()">Change Color</button>
        
    </div>

</template>

<style scoped>
    .redBox {
        background-color: red;
    }
    .blueBox {
        background-color: blue;
    }
    #demo1 {
        color: white;
    }
</style>
