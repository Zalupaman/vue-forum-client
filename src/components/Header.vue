<template>
  <header class="header">
    <div class="container df">
      <nav class="nav">
        <p class="nav-title">Alex`s Forum</p>
        <router-link to="/" class="nav-link linkHover">Home</router-link>
        <router-link to="/" class="nav-link linkHover">Каталог</router-link>
      </nav>
      <div class="sing">
        <router-link to="/auth/login">
          <button class="sign-in">Log In</button>
        </router-link>
        <router-link to="/auth/signup">
          <button class="sign-up">Sign Up</button>
        </router-link>
      </div>
    </div>
  </header>
</template>

<script>
export default {
name: "Header"
}
</script>

<style lang="scss" scoped>
.header {
  width: 100%;
  background: #ffffff;
  padding: 15px;
  box-sizing: border-box;
}
.df {
  @include flex-between;
}
.nav {
  display: flex;
  align-items: center;
  &-title {
   font-size: 24px;
    font-weight: 700;
    padding-right: 10px;
    margin-right: 10px;
    color: $black;
    border-right: 1px #27252540 solid;
  }
  &-link {
    color: $black;
    margin-right: 10px;
    font-weight: 500;
    font-size: 18px;
  }
}
.sign {
  &-in {
    background: none;
    color: $black;
    border-radius: 6px;
    padding: 5px 10px;
    font-weight: 700;
    box-sizing: border-box;
  }
  &-up {
    background: $prim-background;
    color: #ffffff;
    border-radius: 6px;
    padding: 5px 10px;
    font-weight: 700;
    box-sizing: border-box;
  }
}
</style>
