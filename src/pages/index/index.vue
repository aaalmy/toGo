<template>
  <div>
    我是首页
    <ul>
      <li @longtap="delOne(index)" v-for="(item,index) in list">
        {{item.name}}--{{item.skill}}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      list: [
        {
          name: "lmy",
          skill: "唱歌"
        },
        {
          name: "jzf",
          skill: "跳舞"
        },
        {
          name: "lgvd",
          skill: "玩"
        }
      ]
    };
  },
  methods: {
    delOne(index) {
      wx.showModal({
        title: "提示",
        content: "你确定删除吗？"
      });
    }
  }
};
</script>

<style scoped>
</style>

