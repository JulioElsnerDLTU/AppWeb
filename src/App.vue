<script>
    import Welcome from "./components/welcoming/components/welcome.component.vue"
    export default {
        name: 'app',
        components: {Welcome},
        data(){
            return {
                firstName: '',
                lastName: '',
                developerCount: 0
            }
        }
    }
</script>

<template>
    <h1>Hello Vue Dev !</h1>
    <Welcome :firstName="firstName" :lastName="lastName"></Welcome>
</template>
