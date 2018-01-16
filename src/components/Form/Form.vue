<template>
    <form>
        <fullname v-model="form.user.fullname" />

        <div class="form-group">
            <label for="eml">Email</label>
            <input class="form-control" id="eml" v-model="form.user.mail" type="text" />
        </div>

        <div class="form-group">
            <label for="password">Password</label>
            <input class="form-control" id="password" v-model="form.user.password" type="password" />
        </div>

        <div class="form-check">
            <input class="form-check-input" id="storage" v-model="form.allowStorage" type="checkbox" />
            <label class="form-check-label" for="storage">allow Database storage</label>
        </div>

        <button @click.prevent="form.submitted = true" class="btn btn-success">Submit this</button>
    </form>
</template>

<script>
    import Fullname from './Fullname.vue'
    export default {
        props: {
            form: {
                required: true,
                type: Object,
            },
        },
        components: {
            fullname: Fullname,
        }
    }
</script>

<style scoped>
    button {
        margin-top: 20px;
    }
</style>