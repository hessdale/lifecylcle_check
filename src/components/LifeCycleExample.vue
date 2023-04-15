<template>
    <div>

    </div>
</template>

<script>
export default{
    

beforeCreate:function (){
console.log(`before component is mouneted`);
},
created:function () {
    console.log(`component has been created`);
},
beforeMount:function () {
console.log(`before component hase been mounted`);
},
mounted:function () {
    console.log(`component has been mounted`);
},
};
</script>

<style scoped>

</style>