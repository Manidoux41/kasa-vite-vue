<script setup>

const props = defineProps({
    lodging: {
     type: Array,
     required: true
   },
 }) 

 console.log(props.lodging)

</script>

<template>   
        <div v-for="item in lodging" class="card" key="item.id">
            <img :src="item.cover" alt="image" />
            <h3>{{item.title}}</h3>            
        </div>
    
</template>

<style lang="scss" scoped>
    .card{
        position: relative;
        border-radius: 10px;
        overflow: hidden;
        width: 100%;
        height: 280px;
        cursor: pointer;
        @media screen and (min-width: 768px) {
            width: 340px;
            height: 340px;
        }
        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            filter: brightness(.65);
        }
        h3 {
            position: absolute;
            font-size: 14px;
            color: #fff;
            z-index: 1;
            bottom: 12px;
            left: 8px;
        }            
    }
    
</style>
