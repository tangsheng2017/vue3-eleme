<template>
  <div class="inputGroup">
    <!-- 组件结构 -->

    <!-- 组件容器 -->
    <div class="input_group">
      <!-- 输入框 -->
      <input
        :type="text"
        :value="value"
        :placeholder="placeholder"
        :name="name"
        @input="$emit('input',$event.target.value)"
      />
      <!-- 输入框后面的按钮 -->
      <button v-if="!!btnTitle" :disabled="disabled" @click="$emit('btnClick')">{{btnTitle}}</button>
      <!-- 错误提醒 -->
      <div v-if="!!error" class="invalid-feedback">{{error}}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "inputGroup",
  props: {
    type: {
      //表格类型
      type: String,
      default: "text"
    },
    value: String, //绑定值
    placeholder: String, //对应提醒
    name: String,
    btnTitle: String, //是否有获取验证码
    disabled: Boolean, //按钮是否可用
    error: String //验证提醒
  }
};
</script>

<style scoped>
.login {
  width: 100%;
  height: 100%;
  padding: 30px;
  box-sizing: border-box;
  background: #fff;
}

.logo {
  text-align: center;
}
.logo img {
  width: 150px;
}
.text_group,
.login_des,
.login_btn {
  margin-top: 20px;
}
.login_des {
  color: #aaa;
  line-height: 22px;
}
.login_des span {
  color: #4d90fe;
}
.login_btn button {
  width: 100%;
  height: 40px;
  background-color: #48ca38;
  border-radius: 4px;
  color: white;
  font-size: 14px;
  border: none;
  outline: none;
}
.login_btn button[disabled] {
  background-color: #8bda81;
}
</style>