<template>
    <div class="display-border" style="max-width:450px; margin:auto; background: #234; color:white;">
        <p style="font-size:1.5rem" class="bg-dark w-75 m10 font-monospace m-auto p-2" @keypress="updateScreen">{{output}}</p>
    </div>
</template>
<script>
export default {
    name:"DisplayScreen",
    props:{
        output:{
            type:String,
            default:"'0'"
        }
    }
    
}
</script>
<style scoped>
.display-border{
    border-top-left-radius: 5px;
    border-top-right-radius: 5px;
    display: flex;
    justify-content: right;
}
p{
    margin-right: 25px;
}
</style>