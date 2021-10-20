<template>
    <div class="grid">
        <div v-for= "i in 400" :key= "i" class='grid-box'>
            {{i}}
        </div>
    </div>
</template>

<script>
export default {
    name: 'Grid',
    data() {
        return {

        }
    }
}
</script>

<style scoped>
.grid {
    display: grid;
    grid-template-columns: repeat(20, 1fr)
}

.grid-box {
    width: 20px;
    width: 20px;
   border: 1px solid #000;
   
}

</style>