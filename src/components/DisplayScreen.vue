<template>
    <div class="display-border">
        <p>{{output}}</p>
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
    border: 1px solid black;
    border-radius: 5px;
    display: flex;
    justify-content: right;
}
p{
    margin-right: 25px;
}
</style>