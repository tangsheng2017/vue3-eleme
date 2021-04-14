<template>
  <div class="login">
    <div class="logo">
      <img src="../assets/logo.jpg" alt="my login image">
    </div>
    
  </div>
</template>

<script>
import inputGroup from '../components/inputGroup';
export default {
  name:'login',
  data(){
    return{
      phone:'',
      verifyCode:'',
      errors:{},
      btnTitle:'获取验证码',
      disabled:false,
      
    }
  },
  // components:{
  //   'inputGroup':inputGroup
  // }
}
</script>

<style>
.login{
  width: 100%;
  height: 100%;
  padding: 30px;
  box-sizing: border-box;
  background-color: #fff;
  text-align: center;
}

.logo{
  text-align: center;
}
.logo img{
  width: 150px;
}
</style>