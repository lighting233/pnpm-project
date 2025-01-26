<template>
    <button class="my-button">{{ label }}</button>
</template>

<script setup lang="js" name="MyButton">
import useSystemStore from '@/store/main/system/system'
import { formatUTC } from '@/utils/format'
import { BASE_URL } from '../test'
const systemStore = useSystemStore()
const queryInfo = {
    size: 0,
    offset: 20
  }
systemStore.postUserListAction(queryInfo)
const props = defineProps({
    label: {
        type: String,
        default: '这是定义在全局的MyButton组件'
    }
});
</script>

<style scoped>
.my-button {
    background-color: rgb(228, 13, 13);
    color: white;
    border: none;
    padding: 10px 20px;
    cursor: pointer;
}
</style>
