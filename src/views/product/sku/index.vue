<template>
    <el-card>
        <el-table border style="margin: 10px 0px;">
            <el-table-column label="序号" type="index" align="center" width="80px"></el-table-column>
            <el-table-column label="名称" show-overflow-tooltip width="150px"></el-table-column>
            <el-table-column label="描述" show-overflow-tooltip width="150px"></el-table-column>
            <el-table-column label="图片" width="150px"></el-table-column>
            <el-table-column label="重量" width="150px"></el-table-column>
            <el-table-column label="价格" width="150px"></el-table-column>
            <el-table-column label="操作" width="150px" fixed="right"></el-table-column>
        </el-table>
        <el-pagination v-model:current-page="pageNO" v-model:page-size="pageSize" :page-sizes="[10, 20, 30, 40]"
            :background="true" layout="prev, pager, next, jumper,->,total, sizes, " :total="400" />
    </el-card>
</template>

<script lang='ts' setup>
import { ref } from 'vue'
// SPU是一类产品，SKU是产品之下的属性

//分页器当前页码
let pageNO = ref<number>(1);
//每一页展示几条数据
let pageSize = ref<number>(10);
</script>

<style scoped></style>