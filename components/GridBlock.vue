<script setup>
import { ref } from 'vue';

const props = defineProps({
    classNames: {
        type: String,
    },
})

const classNames = ref(props.classNames?.split(" ") ?? []);
if (!classNames.value.some(v => /grid-cols-*/.test(v))) {
    classNames.value.push('grid-cols-2');
}
</script>

<template>
    <div class="h-full grid" :class="classNames">
        <slot />
    </div>
</template>