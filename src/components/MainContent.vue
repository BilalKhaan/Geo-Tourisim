<template>
  <div class="main-content">
    <div class="banner">
      <img src="@/assets/images/banner.jpg" />
    </div>
    <div class="cover">
      <img src="@/assets/images/Preview.png" />
      <span>Set Cover</span>
    </div>
    <div class="heading">
      <p >
        A walking trail of Montmartre, Paris
      </p>
    </div>
    <div class="content">
      <p>Dominated by the grandeur of the ever-visible Sacré-Cœur Basilica, the leafy hilltop village of Montmartre was once the play area of Paris’s most famous artists, bohemians and creatures of the night. These days, the winding cobbled streets host chic cafes, retro boutiques and fine French dining but, if you look closely enough, those in search of historical secrets can still find traces of the old La Bohème hidden between the tourist traps…</p>
    </div>
    <div class="tags">
      <span class="title"> Tags </span>
      <div class="tag-list flex-only">
        <div class="add-tag">
          <span><img src="@/assets/images/Preview.png" /></span>
        </div>
        <div class="tag flex-between" v-for="tag in tags" :key="tag.id">
          <span>{{tag.name}}</span>
          <img src="@/assets/images/Preview.png" />
        </div>
      </div>
    </div>
    <categories />
  </div>
</template>
<script>
import Categories from "./Categories.vue"
export default {
  components: {
    Categories
  },
  data () {
   return {
     tags: [{
       id: 1,
       name: 'Montmartre'
     }, {
       id: 2,
       name: 'Paris'
     }]
   }
  }
}
</script>
<style lang="scss" scoped>
.main-content {
  width: 49.5%;
  margin-top: 25px;
  position: relative;
  .banner {
    img {
      width: 100%;
      height: 220px;
      border-radius: 10px;
      object-fit: cover;
    }
  }
  .cover {
    display: flex;
    position: absolute;
    top: 177px;
    left: 19px;
    cursor: pointer;
    img {
      margin-right: 30px;
    }
    span {
      color: #FFFFFF;
      font-family: "Avenir";
      font-size: 17px;
      font-weight: 500;
      letter-spacing: 0;
      line-height: 24px;
    }
  }
  .heading {
    color: #212121;
    font-family: "Avenir";
    font-size: 36px;
    font-weight: bold;
    letter-spacing: 0.54px;
    line-height: 42px;
    margin: 20px 0px 30px 0px;
    border-bottom: 1px dashed #eee;
    p {
      padding-bottom: 20px;
      margin: 0;
    }
  }
  .content {
    color: #5B5C5E;
    font-family: "Avenir";
    font-size: 18px;
    font-weight: 300;
    letter-spacing: 0;
    line-height: 32px;
    border-bottom: 1px dashed #eee;
    p {
      padding-bottom: 20px;
      margin: 0;
    }
  }
  .tags {
    margin-top: 18px;
    .title {
      color: #373A3E;
      font-family: "Avenir";
      font-size: 20px;
      font-weight: 900;
      letter-spacing: 0;
      line-height: 28px;
    }
    .tag-list {
      margin-top: 6px;
      padding: 27px 0px;
      .add-tag {
        box-sizing: border-box;
        height: 32px;
        width: 32px;
        border: 1px solid #BCDEE8;
        border-radius: 32px;
        background-color: #F8FBFC;
        border-radius: 50%;
        margin-right: 20px;
        span {
          display: flex;
          justify-content: center;
          padding: 3px 0px;
        }
      }
      .tag {
        border: 1px solid #BCDEE8;
        border-radius: 32px;
        background-color: #F8FBFC;
        padding: 0px 10px 0px 12px;
        margin-right: 20px;
        span {
          opacity: 0.8;
          color: #373A3E;
          font-family: Avenir;
          font-size: 16px;
          font-weight: 300;
          letter-spacing: 0;
          line-height: 22px;
        }
        img {
          padding-left: 10px;
        }
      }
    }
  }
}
</style>