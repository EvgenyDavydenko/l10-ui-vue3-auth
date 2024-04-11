<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card">
                    <div class="card-header">Home Component</div>

                    <div class="card-body">
                        I'm an home component.
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import axios from 'axios';  
    export default {
        mounted() {
            axios.get('/api/hello').then(r => {
                console.log(r.data);
            }).catch(error => {
                console.log(error.response.data.errors);
            })
        }
    }
</script>
