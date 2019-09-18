<template>
  <vue-drag-infinite :json="json" :name="name" @save="saveJson"></vue-drag-infinite>
</template>

<script>
import vueDragInfinite from 'vue-drag-infinite'
import mock from "mockjs"

export default {
  data () {
    return {
      name: 'drag',//默认标题文字
      json: [//默认div块的信息 为空的时候只能新增不能修改
        {
          style: {
            width: "150px",
            height: "150px",
            fontSize: "14px",
            color: "#fff",
            left: "50px",
            backgroundColor: "#999"
          },
          text: '这是第一个div'
        },
      ],
    }
  },
  components: {
    "vue-drag-infinite": vueDragInfinite
  },
  methods: {
    saveJson (obj) {
      console.log(obj)
    }
  }
}
</script>