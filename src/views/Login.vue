<template>
  <div class="login">
    <b-jumbotron  header="Vue.js 聊天室"
                  lead="Demo 通过 Chatkit SDK 和 Bootstrap-Vue 创建"
                  bg-variant="info"
                  text-variant="white">
      <b-btn target="_blank" href="https://pusher.com/chatkit">👀参考自此网站</b-btn>
      <span style="padding:5px"></span>
      <b-btn target="_blank" href="https://www.sitepoint.com/community">👀还有他</b-btn>
    </b-jumbotron>
    <b-container>
      <b-row>
        <b-col lg="4" md="3"></b-col>
        <b-col lg="4" md="6">
          <LoginForm />
        </b-col>
        <b-col lg="4" md="3"></b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import LoginForm from '@/components/LoginForm.vue'

export default {
  name: 'login',
  components: {
    LoginForm
  }
}
</script>