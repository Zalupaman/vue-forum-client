<template>
  <div class="auth-wrapper">
    <div class="auth">
      <p class="auth-title">{{ $route.params.type === 'login' ? 'Логин' : 'Регистрация' }}</p>
      <form class="auth-content">
        <input type="text" placeholder="Логин" class="auth-inp" v-model="login">
        <input type="text" placeholder="Пароль" class="auth-inp" v-model="password">
        <button class="auth-btn">Войти</button>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: "Auth",
  data() {
    return {
      login: '',
      password: ''
    }
  }
}
</script>

<style lang="scss" scoped>
.auth {
  background: #ffffff;
  border-radius: 10px;
  width: 300px;
  padding: 25px;
  &-wrapper{
    width: 100%;
    height: 91vh;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  &-content {
    display: flex;
    flex-direction: column;
  }
  &-title {
    font-size: 24px;
    color: $black;
    margin-bottom: 15px;
    margin-top: 0;
    font-weight: bold;
    text-align: center;
  }
  &-inp {
    padding: 15px;
    box-sizing: border-box;
    outline: none;
    margin-bottom: 10px;
    border: none;
    border-bottom: 1px $prim-background solid;
  }
  &-btn {
    padding: 10px;
    background: $prim-background;
    border-radius: 6px;
    font-size: 18px;
    font-weight: 700;
    color: #ffffff;
  }
}
</style>
