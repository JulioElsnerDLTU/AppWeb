<script>      
    import {Developer} from "../model/developer.entity.js";
    export default {
        name: 'welcome',
        props: {
            firstName: String,
            lastname: String
        },
        methods:{
            developerName(){
                let developer = new Developer(this.firstName, this.lastname);
                return developer.getFullName();
            }
        }
    }
</script>

<template>
    <p>Hello {{developerName()}} . Now you are a vue developer</p>
</template>
    
