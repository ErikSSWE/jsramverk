<template>
    <div class="toolbar">
        <button @click="save" class="btn">Save</button>
        <div id="app">
            <ckeditor :editor="editor" v-model="editorData" :config="editorConfig"></ckeditor>
        </div>
    </div>
</template>

<script>
    import ClassicEditor from '@ckeditor/ckeditor5-build-classic';

    export default {
        name: 'app',
        data() {
            return {
                editor: ClassicEditor,
                editorData: 'Write text here',
                editorConfig: {
                    //toolbar: [ 'bold']
                },
            };
        },
        methods: {
            save() {
                console.log(this.editorData);
            }
        }
    }

</script>

<style scoped>
.btn {
    border: 1px solid black;
    max-width: 60px;
    border-radius: 2px;

}

.btn:hover {
    background-color: lightgray;
}

</style>