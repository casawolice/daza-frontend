<template>
  <validator name="validation">
    <form novalidate @submit.prevent="submit()">
      <div class="form-group row" style="display: none;">
        <label for="mobile-input" class="col-xs-3 col-sm-2 col-form-label">手机</label>
        <div class="col-xs-9 col-sm-10">
          <label class="form-control-static">{{ user.mobile }}</label>
        </div>
      </div>
      <div class="form-group row">
        <label for="password-input" class="col-xs-3 col-sm-2 col-form-label">帐号密码</label>
        <div class="col-xs-9 col-sm-10">
          <p class="form-control-static">
            <a href="#">修改密码</a>
          </p>
        </div>
      </div>
      <div class="form-group row" style="display: none;">
        <label for="bio-input" class="col-xs-3 col-sm-2 col-form-label">社交帐号</label>
        <div class="col-xs-9 col-sm-10">
          <p class="form-control-static">
            <a href="#"> 绑定微信</a>
            <a href="#"> 绑定微信</a>
            <a href="#"> 绑定GitHub</a>
          </p>
        </div>
      </div>
      <hr style="display: none;">
      <div class="form-group" style="display: none;">
        <button type="submit" class="btn btn-primary">保存</button>
      </div>
    </form>
  </validator>
</template>

<script>
import { auth } from '../../vuex/getters';
import { updateProfile } from '../../vuex/actions';

export default {
  vuex: {
    getters: {
      auth,
    },
    actions: {
      updateProfile,
    },
  },
  data() {
    return {
      user: this.auth.user,
    };
  },
  ready() {
  },
  methods: {
    submit() {
    },
  },
};
</script>

<style scoped>
</style>
