<template>
    <div class="hidden lg:fixed lg:inset-y-0 lg:z-50 lg:flex lg:w-72 lg:flex-col">
        <SidebarContent
            :navigation="navigation"
            :isAdmin="isAdmin"
            :showSettings="showSettings"
            :logo="logo"
        />
    </div>
</template>

<script setup>
    import SidebarContent from './SidebarContent.vue';

    defineProps({
        navigation: {
            type: Array,
            required: true,
        },
        isAdmin: {
            type: Boolean,
            default: false,
        },
        showSettings: {
            type: Boolean,
            default: true,
        },
        logo: {
            type: Object,
            default: () => ({
                src: 'https://tailwindui.com/plus/img/logos/mark.svg?color=indigo&shade=600',
                alt: 'Your Company',
            }),
        },
    });
</script>
