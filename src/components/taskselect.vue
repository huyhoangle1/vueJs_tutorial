<template>
    <div>
<div class ="list">
    <div v-for="(language,index) in languages" :key="index">
        <span>
            {{language.name}}
        </span>
    </div>
</div>
    </div>
</template>
<script>
    export default{
        data(){
            return{
                language:[
                    {name :'php',selected:false },
                    {name :'java',selected:false },
                    {name :'html',selected:false },
                    {name :'css',selected:false },
                    {name :'vúejs',selected:false }
                ]
            }
        }
    }
</script>
<style lang= "scss">

</style>