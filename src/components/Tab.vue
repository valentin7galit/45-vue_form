<template>
    <div v-show="active"><slot></slot></div>
</template>

<script>
export default {
    name: "Tab",
    props: {
        name: { 
            required: true 
        },
        selected: {
            default: false
        }
    },
    data() {
        return {
            active: false
        };
    },
    mounted() {
        this.active = this.selected;
    }
}
</script>