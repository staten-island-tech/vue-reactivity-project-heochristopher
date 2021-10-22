<template>
    <div class="grid">
        <div v-for= "i in 400" :key= "i" class='grid-box' @click="fillBox()"></div>
    </div>
</template>

<script>
export default {
    name: 'Grid',
    data() {
        return {

        }
    },
    methods: {
        fillBox() {
            console.log('hey')
        }
    }
}
</script>

<style scoped>
.grid {
    display: grid;
    grid-template-columns: repeat(20, 1fr);
    grid-column-gap: 0px;
    width: 60%;

}

.grid-box {
    padding: 0px;
    margin: 0px;
    height: 27.1px;
    width: 27.1px;
   border: 1px solid #000;
   
}

</style>