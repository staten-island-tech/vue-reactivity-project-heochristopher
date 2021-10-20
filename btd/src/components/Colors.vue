<template>
    <div class="grid">
        <div v-for= 'color in colors' :key= 'color' class='color-box' :id='`${color}`'> 
            {{color}}
        </div>
    </div>
</template>

<script>
export default {
    name: 'Colors',
    data() {
        return {
            colors: ['blue', 'red', 'yellow', 'green', 
            'black', 'purple', 'orange', 'pink']
        }
    }
}
</script>