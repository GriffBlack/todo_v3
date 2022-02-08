<template>
    <div class="t-input my-list">
        <input ref="title"  :model='title' placeholder="Title" type="text">
        <input ref="description"  :model='description' placeholder="Description" type="text">
        <button>Add task</button>
    </div>
</template>
<script>
import { ref } from 'vue';

export default {
    setup() {
       const title = ref('');
       const description = ref('');

       return {
           title,
           description
       }
    }
}
</script>
<style>
    .t-input{
        margin: 10px 0;
    }
</style>