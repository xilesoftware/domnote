<script lang="ts">
// import { storageDemo } from '~/logic/storage'
import { useStorageLocal } from '~/composables/useStorageLocal'

export default {
    name: "OptionsPage",

    props: {
    },

    emits: [],

    mounted() {
    },

    computed: {
    },

    methods: {
        saveToStorage(key: string, value: string) {
            console.log("SAVE TO STORAGE: ", key, value);
            useStorageLocal(key, value)
            // useStorageLocal(key, value, { listenToStorageChanges: true })
        }
    }
};
</script>

<template>
    <main class="px-4 py-10 text-center text-gray-700 dark:text-gray-200">
        <img src="/assets/icon.svg" class="icon-btn mx-2 text-2xl" alt="extension icon">
        <div>Options</div>
        <p class="mt-2 opacity-50">
            This is the options page
        </p>

        <!-- <input v-model="storageDemo" class="border border-gray-400 rounded px-2 py-1 mt-2"> -->


        <button @click="saveToStorage('test', '123')">[SAVE-ICON]</button>

        <div class="mt-4">
            Powered by Vite
            <pixelarticons-zap class="align-middle" />
        </div>
    </main>
</template>

<script setup lang="ts">
    import { storageDemo } from '~/logic/storage'
</script>
