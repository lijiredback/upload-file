<template>
    <div class="upload">
        <!-- 上传控件 -->
        <input type="file" @change="handleFileChange" />
        <el-button type="primary" size="small" @click="handleUpload">点击上传</el-button>
    </div>
</template>

<script>
export default {
    name: 'UploadFile',
    data() {
        return {
            container: {
                file: null
            }
        }
    },
    methods: {
        // addEventListener for input file changed
        handleFileChange(e) {
            // console.log(e)
            const [file] = e.target.files

            if (!file) return

            Object.assign(this.$data, this.$options.data())
            this.container.file = file
        },
        // click button to upload file
        async handleUpload() {
            
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
