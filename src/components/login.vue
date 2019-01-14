<template>
  <div class="login">
     
    <el-form label-position="top" label-width="80px" :model="formData" class="form">
         <h2>用户登录</h2>
      <el-form-item label="用户名">
        <el-input v-model="formData.username"></el-input>
      </el-form-item>
      <el-form-item label="密码">
        <el-input v-model="formData.password"></el-input>
      </el-form-item>
      <el-button type="primary" class="btn" @click="getFormData()">登录</el-button>
    </el-form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      formData: {
        username: "",
        password: ""
      }
    }
  },
  methods: {
    //   发送请求
    async getFormData () {
            const res = await this.$http.post(`login`,this.formData)
            const {meta:{status,msg},data} = res.data
            console.log(res)
            console.log(status)
            if(status == 200) {
                this.$message(msg)
                this.$router.push({
                    name: "home"
                })
            }
        }
  }
};
</script>

<style>
.login {
  height: 100%;
  background-color: #324152;
  display: flex;
    justify-content: center;
    align-items: center;
}
.login h2 {
  margin-bottom: 20px;
}
.login .form {
    background-color: #fff;
    height: 400px;
    width: 500px;
    padding: 20px;
    border-radius: 10px;
}
.login .form .btn {
    width: 100%;
    margin-top: 30px;
}
</style>
