<template>
    <div class="grid">
        <div v-for= "i in 400" :key= "i" class='grid-box' @click="fillBox(i)" :id='`${i}`'></div>
        <input @keyup.space='fillBox("tool")'>
    </div>
</template>

<script>
export default {
    name: 'Grid',
    props: {
        gridColor: String
    },
    data() {
        return {
          
        }
    },
    methods: {
        fillBox(box) {
            if(box == "tool") {
                document.getElementById(box).style.backgroundColor = '#ffffff'
            }
            document.getElementById(box).style.backgroundColor = this.gridColor
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