<template>
    <div class="container">
        <form class="mtop">
            <div class="row">
                <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
                    <!-- Exercise 1 -->
                    <!-- Create a Signup Form where you retrieve the following Information -->
                    <!-- Full Name (First Name + Last Name) -->
                    <!-- Mail -->
                    <!-- Password -->
                    <!-- Store Data? Yes/No -->
                    <app-form v-if="!myForm.submitted" :form="myForm" />
                    <!-- Exercise 2 -->
                    <!-- Only display the Form if it has NOT been submitted -->
                    <!-- Display the Data Summary ONCE the Form HAS been submitted -->

                    <!-- Exercise 3 -->
                    <!-- Edit the Example from above and create a custom "Full Name" Control -->
                    <!-- which still holds the First Name and Last Name Input Field -->
                </div>
            </div>
        </form>
        <hr>
        <div class="row" v-if="myForm.submitted">
            <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
                <div class="panel panel-default">
                    <div class="panel-heading">
                        <h4>Your Data</h4>
                    </div>
                    <div class="panel-body">
                        <p>Full Name: {{myForm.user.fullname}}</p>
                        <p>Mail: {{myForm.user.mail}}</p>
                        <p>Password: {{myForm.user.password}}</p>
                        <p>Store in Database?: {{myForm.allowStorage}}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import Form from './components/Form/Form.vue';
    export default {
        data() {
            return {
                myForm: {
                    user: {
                        fullname: '',
                        mail: '',
                        password: '',
                    },
                    allowStorage: false,
                    submitted: false,
                }
            }
        },
        components: {
            appForm: Form,
        }
    }
</script>

<style scoped>
.mtop {
    margin-top: 60px;
}
</style>
