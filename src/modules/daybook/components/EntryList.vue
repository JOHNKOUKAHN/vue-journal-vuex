<template>
    <div class="entry-list-container">
        <div class="px-2 pt-2">
            <input 
                type="text"
                class="form-control"
                placeholder="Buescar Entrada">
        </div>

        <div class="entry-scroll-area">
            <Entry
                v-for="item in 100" 
                :key="item" />
        </div>

    </div>
</template>

<script>

import {defineAsyncComponent} from 'vue'
export default {
    components: {
        Entry: defineAsyncComponent( ()  => import('./Entry.vue'))

    }
}
</script>

<style lang="scss" scoped>
    .entry-list-container {
        border-right: 1px solid #2e3c50;
        height: calc( 100vh - 56px);
    }   

    .entry-scroll-area {
        height: calc( 100vh - 110px);
        overflow: scroll;
    }

</style>