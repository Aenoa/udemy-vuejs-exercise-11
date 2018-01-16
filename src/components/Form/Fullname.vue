<template>
    <div class="form-group">
        <label for="fname">Full Name (First + last name)</label>
        <input class="form-control" id="fname" @input="changedValue" v-model="value" type="text" />
    </div>
</template>

<script>
    export default {
        props: ['value'],
        methods: {
            changedValue(v) {
                this.$emit('input', this.value);
            }
        }
    }
</script>

<style scoped>
    
</style>