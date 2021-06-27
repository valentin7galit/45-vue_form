<template>
    <div :class="[alert, alertType]" v-show="openAlert">
        <div class="row">
            <slot></slot>
            <button @click="closeAlert" :class="[buttonType]" class="col-1"><strong>x</strong></button>
        </div>
    </div>
</template>

<script>
export default {
    name: "Alert",
    props: {
        type: {
        type: String,
        required: true,
            validator: function (value) {
                return ['success', 'error', 'danger', 'warning'].indexOf(value) !== -1;
            }
        }
    },
    computed: {
        alertType() {
            return `alert-${this.type}`;
        },
        /* Homework */
        openAlert() {
            return !this.alertVidible;
        },
        buttonType() {
            return `button-${this.type}`;
        }
    },
    data() {
        return {
            alert: 'alert',
            /* Homework */
            alertVidible : false
        }
    },
    /* Homework */
    methods: {
        closeAlert() { 
            this.alertVidible = true;
        }
    }
}
</script>

<style scoped>
.alert {
    border: 1px solid transparent;
    border-radius: 5px;
}
.alert-success {
    color: #155724;
    background-color: #d4edda;
    border-color: #c3e6cb;
}
.alert-error {
    color: #1b1e21;
    background-color: #d6d8d9;
    border-color: #c6c8ca;
}
.alert-danger {
    color: #721c24;
    background-color: #f8d7da;
    border-color: #f5c6cb;
}
.alert-warning {
    color: #856404;
    background-color: #fff3cd;
    border-color: #ffeeba;
}
.button-success {
    color: #155724;
    border: 1px solid #c3e6cb;
}
.button-error {
    color: #1b1e21;
    border: 1px solid #c6c8ca;
}
.button-danger {
    color: #721c24;
    border: 1px solid #f5c6cb;
}
.button-warning {
    color: #856404;
    border: 1px solid #ffeeba;
}
.button-success, .button-error, .button-danger, .button-warning {
    background-color: #fff;
    border-radius: 5px;
}
</style>