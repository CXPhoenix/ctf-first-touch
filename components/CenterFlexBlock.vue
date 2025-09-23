<script setup>
import { useSlideContext } from '@slidev/client';

const props = defineProps({
    isRow: {
        type: Boolean,
        default: false,
    },
    classNames: {
        type: String
    }
})

const classNames = props.classNames?.split(" ").reduce((a, v) => ({...a, [v]: true}), {}) ?? {};
const isRow = useSlideContext().$frontmatter.isRow ?? props.isRow
classNames['flex-col'] = !isRow;
</script>

<template>
    <div class="h-full flex justify-center items-center" :class="classNames">
        <slot />
    </div>
</template>