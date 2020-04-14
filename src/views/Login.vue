<template>
  <el-card class="box-card" id='loginBox'>
    <div slot="header" class="clearfix">
      <span>登录</span>
    </div>
    <el-row>
      <el-input v-model="form.username" placeholder="用户名"></el-input>
    </el-row>
    <el-row>
      <el-input v-model="form.password" placeholder="密码"></el-input>
    </el-row>
    <el-row>
      <el-button type="primary" @click="onSubmit" style="width: 100%;">登录</el-button>
    </el-row>
  </el-card>
</template>

<script>
export default {
  name: 'Login',
  props: {
    msg: String
  },
  data () {
    return {
      form: {
        name: '',
        password: ''
      }
    }
  },
  methods: {
    onSubmit () {
      this.$router.push({ path: '/index' })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  #loginBox{
    margin: 200px auto;
  }
  .el-row {
    margin-bottom: 20px;
    &:last-child {
      margin-bottom: 0;
    }
  }
 .text {
    font-size: 14px;
  }

  .item {
    margin-bottom: 18px;
  }

  .clearfix:before,
  .clearfix:after {
    display: table;
    content: "";
  }
  .clearfix:after {
    clear: both
  }

  .box-card {
    width: 420px;
  }
</style>
