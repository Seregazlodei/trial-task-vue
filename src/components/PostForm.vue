<template>
    <form @submit.prevent="submit">
        <b-form-input placeholder="title"></b-form-input>
        <b-form-input placeholder="body"></b-form-input>
        <b-button variant="dark" type="submit">Create Post</b-button>
        <hr>
    </form>
</template>

<script>
import {mapMutations} from 'vuex'
export default {
    data() {
        return {
            title: '',
            body: ''
        }
    },
    methods: {
        ...mapMutations(['createPost']),
        submit() {
            this.createPost({
                title: this.title,
                body: this.body,
                id: Date.now()
            });
            this.title = this.body = '';
        }
    }
}
</script>

<style scoped>
input {
    display: block;
    width: 100%;
    border: 1px solid #ccc;
    border-radius: 2px;
    padding: 10px;
    margin-bottom: 10px;
}
</style>