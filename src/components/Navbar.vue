<template>
  <div class="navbar flex-between">
    <div class="logo">
      <img src="@/assets/logo.png" />
    </div>
    <div class="nav-links flex-between">
      <a class="discover" href="#"> Discover </a> 
      <a class="create" href="#"> Create </a>
      <span class="download" type="button"> Download </span>
    </div>
    <div class="nav-icons justify-end">
      <div class="nav-icons-right flex-between">
        <img src="@/assets/images/Preview.png" />
        <img src="@/assets/images/Preview.png" />
        <img src="@/assets/images/Preview.png" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>
<style lang="scss" scoped>
.navbar {
  background-color: #FFFFFF;
  padding: 8px 25px;
  box-shadow: inset 0 -0.5px 0 0 rgba(200,199,204,0.5), 0 2px 6px 0 rgba(211,220,224,0.2);
  .logo {
    width: 30%;
    img {
      height: 56px;
    }
  }
  .nav-links {
    width: 25%;
    font-family: "Lato";
    font-size: 17px;
    font-weight: 500;
    letter-spacing: 0;
    line-height: 23px;
    a {
      text-decoration: none;
    }
    .discover {
      color: #5B5C5E;
    }
    .create {
      color: #2DAEE1
    }
    .download {
      color: white;
      border-radius: 24px;
      background-color: #BDBFC2;
      padding: 7px 19px;
      cursor: pointer;
    }
  }
  .nav-icons {
    width: 30%;
    .nav-icons-right {
      width: 40%;
    }
  }
}
@media  (min-width: 768px) and (max-width: 1023px)  {
  .navbar {
    .nav-links {
      width: 35%;
    }
  }
}
@media (max-width: 768px)  {
  .navbar {
    .nav-links {
      width: 45%;
    }
  }
}
</style>
