<template>
  <div class="login-form">
    <h5 class="text-center">登录</h5>
    <hr>
    <b-form @submit.prevent="onSubmit">
       <b-alert variant="danger" :show="hasError">{{ error }} </b-alert>

      <b-form-group id="userInputGroup"
                    label="用户名"
                    label-for="userInput">
        <b-form-input id="userInput"
                      type="text"
                      placeholder="输入用户名"
                      v-model="userId"
                      autocomplete="off"
                      :disabled="loading"
                      required>
        </b-form-input>
      </b-form-group>

      <b-button type="submit"
                variant="primary"
                class="ld-ext-right"
                v-bind:class="{ running: loading }"
                :disabled="isValid">
                登录 <div class="ld ld-ring ld-spin"></div>
      </b-button>
    </b-form>

    <p class="tips">注册用户请联系qq:1079771176</p>
  </div>
</template>

<script>

import { mapState, mapGetters, mapActions } from 'vuex'
export default {
  name: 'login-form',
  data() {
    return {
      userId: '',
    }
  },
  computed: {
    isValid: function() {
      const result = this.userId.length < 3;
      return result ? result : this.loading
    },
    ...mapState([
      'loading',
      'error'
    ]),
    ...mapGetters([
      'hasError'
    ])
  },
   methods: {
    ...mapActions([
      'login'
    ]),
    async onSubmit() {
      const result = await this.login(this.userId);
      if(result) {
        this.$router.push('chat');
      }
    }
  }
}
</script>

<style>
  .tips{
    color:red;
    position: relative;
    top:40px;
    left:50px;
  }
</style>