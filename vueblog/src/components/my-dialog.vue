<template>
    <el-dialog title="选择水果" :visible.sync="dialogVisible" width="30%">
        <div>弹窗内容</div>
 
        <span slot="footer">
            <el-button @click="toggleDialog('dialogVisible', false)">取 消</el-button>
            <el-button type="primary" @click="handleOk">确 定</el-button>
        </span>
    </el-dialog>
 
</template>
 
<script>
export default {
    props: {
        visible: Boolean,
    },
    data() {
        return {};
    },
    computed: {
        dialogVisible: {
            get() {
                return this.visible;
            },
            set(val) {
                this.$emit('update:visible', val);
            },
        },
    },
    methods: {
        toggleDialog(key, visible) {
            this[key] = visible;
        },
        handleOk() {},
    },
};
</script>
 
<style lang="less" scoped>
</style>