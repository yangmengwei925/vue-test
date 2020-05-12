<template>
  <div class="hello">
    <div class="box">
      我是子组件
      <button @click="flag=!flag">点击显示弹框</button>
      <div v-show="flag" class="pop">
        <!-- <input type="text" v-model="val" /> -->
        <ul>
          <li v-for="(item,index) in list" v-bind:key="index">
            <input v-model="item.flag" type="checkbox">
            {{item.title}}
          </li>
        </ul>
        <div>
          <button @click="sendMsg">确定提交</button>
          <button @click="val=''">取消提交</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  data() {
    return {
      val: "",
      flag: true,
      list: [
        {
          title: "语文",
          flag:true,
        },
        {
          title: "化学",
          flag:true,
        },
        {
          title: "数学",
          flag:true,
        },
        {
          title: "生物",
          flag:false
        }
      ]
    };
  },
  methods: {
    sendMsg() {
      this.$emit("send", this.list);
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.box {
  width: 100%;
  height: 200px;
  background: #ccc;
}
</style>
