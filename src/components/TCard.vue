<template>
    <div class="t-card my-style">
        <div>
            <h3>{{model.title}}</h3>
            <p>{{model.description}}</p>
        </div>
        <div>
            <button @click="emitOnDone" v-if="!model.status">✅</button>
            <button @click="emitOnRemove" v-else>❌</button>
        </div>
    </div>
</template>
<script>
export default {
    props: {
        model: {
            required: true,
            default: {
                id: 0,
                title: 'To do something',
                description: 'And upload on GitHub',
                status: false
            }
        }
    },

    setup(props, { emit }) {
        const emitOnDone = () => {
            emit('onDone')
        }
        
        const emitOnRemove = () => {
            emit('onRemove')
        }
        return {
            emitOnDone,
            emitOnRemove
        }
    }
    
}
</script>
<style>
.t-card{
    display: flex;
    justify-content: space-between;
    align-items: center;
}
    
</style>