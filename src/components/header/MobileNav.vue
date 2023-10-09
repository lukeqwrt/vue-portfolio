<script setup>
    const props = defineProps(['toggleActive'])
    import NavItems from './NavItems.vue';
</script>

<template>
    <Transition 
        enter-active-class="duration-300 ease-out"
        enter-from-class="transform opacity-0"
        enter-to-class="opacity-100"
        leave-active-class="duration-200 ease-in"
        leave-from-class="opacity-100"
        leave-to-class="transform opacity-0"
    >
        <div v-if="props.toggleActive" class="modal_nav_container md:hidden fixed left-0 top-0 bg-white w-full h-full p-5 z-10 dark:bg-[#121212]">
            <div class="modal-wrapper mt-12"> 
                <NavItems class="grid gap-7 text-center " />
            </div>
        </div>
    </Transition>
</template>