<template>
    <div class="upload">
        <input type="file" @change="handleFileChange" />
        <el-button type="primary" size="small">点击上传</el-button>
    </div>
</template>

<script>
export default {
    name: 'UploadFile',
    data() {
        return {}
    },
    methods: {
        // addEventListener for input file changed
        handleFileChange(e) {
            console.log(e)
        }
    }
}
</script>

<style scoped>
    .upload {
        width: 500px;
        height: 300px;
        margin: 200px auto;
        border: 1px solid #ccc;
        text-align: center;
        line-height: 300px;
    }
</style>
