<template>
  <el-container direction="vertical">
    <el-row type="flex" justify="center" align="middle" style="min-height: 100vh;">
      <el-col :md="10" :xs="20">
        <el-card>
          <div>
            <h1>Login</h1>
            <span>Sign in to your account</span>
          </div>
          <el-form ref="form" :model="form">
            <el-form-item label="Email:">
              <el-input v-model="form.email" type="email"></el-input>
            </el-form-item>
            <el-form-item label="Password:">
              <el-input v-model="form.name" type="password"></el-input>
            </el-form-item>
            <el-form-item>
              <el-button type="primary" @click="onSubmit">Login</el-button>
            </el-form-item>
          </el-form>
        </el-card>
      </el-col>
    </el-row>
  </el-container>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      form: {
        email: "",
        password: ""
      }
    };
  },
  methods: {
    onSubmit(e) {
      e.preventDefault();
      console.log("submit!");
    }
  }
};
</script>

<style>
</style>
