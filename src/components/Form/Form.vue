<template>
    <form>
        <div class="form-group">
            <label for="fname">First Name</label>
            <input class="form-control" id="fname" v-model="form.user.fname" type="text" />
        </div>
        <div class="form-group">
            <label for="lname">Last Name</label>
            <input class="form-control" id="lname" v-model="form.user.lname" type="text" />
        </div>

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
    export default {
        props: {
            form: {
                required: true,
                type: Object,
            },
        },
        methods: {
            
        }
    }
</script>

<style scoped>
    button {
        margin-top: 20px;
    }
</style>