<template>
  <div>
    <div class="body flex-between">
      <div class="description">
        <p> Description </p>
      </div>
      <div class="links-and-btn flex-between">
        <div class="tabs flex-between">
          <div v-for="lang in language" :key="lang.id" :class="{'active-border': activeTab == lang.name}">
            <p 
             :class="{'active': activeTab == lang.name}"
            @click="activeTab=lang.name"> {{ lang.name }} </p>
          </div>
        </div>
        <div class="add">
          <div class="flex-between">
            <img src="@/assets/images/Preview.png" />
            <span>Add...</span>
          </div>
        </div>
      </div>
      <div style="width: 20%;"></div>
    </div>

  </div>
</template>

<script>

export default {
  data () {
    return {
      activeTab: 'English',
      language: [{
        id: 1,
        name: 'English'
      }, {
        id: 2,
        name: 'French'
      }, {
        id: 3,
        name: 'Dutch'
      }, {
        id: 4,
        name: 'Spanish'
      },]
    }
  }
}
</script>
<style lang="scss" scoped>
.body {
  padding: 8px 0px;
  .description {
    width: 23%;
    padding-left: 25px;
    padding-bottom: 17px;
    p {
      color: #373A3E;
      font-family: "Avenir";
      font-size: 20px;
      font-weight: 900;
      letter-spacing: 0;
      line-height: 28px;
      padding-top: 19px;
      
    }
  }
  .links-and-btn {
    width: 48.5%;
    .tabs {
      width: 48%; 
      div {
        width: 76px;
        text-align: center;
        p {
          opacity: 0.7;
          color: #373A3E;
          font-family: "Avenir";
          font-size: 15px;
          font-weight: 500;
          letter-spacing: 0;
          line-height: 22px;
          text-align: center;
          cursor: pointer;
        }
        .active {
          font-family: "Avenir";
          font-size: 15px;
          font-weight: 500;
          letter-spacing: 0;
          line-height: 22px;
          text-align: center;
          color: #2DAEE1;
          cursor: pointer;
        }
      }
      .active-border {
        border-bottom: 2px solid #2DAEE1;
      }
    }
    .add {
      div {
        img {
          margin-right: 13px;
        }
        color: #84898D;
        font-family: "Avenir";
        font-size: 14px;
        font-weight: 500;
        letter-spacing: 0;
        line-height: 19px;
        box-sizing: border-box;
        border: 1px solid #BCDEE8;
        border-radius: 24px;
        background-color: #F8FBFC;
        padding: 11px 25px 11px 20px;
        cursor: pointer;
      }
    }
  }
}
@media  (min-width: 768px) and (max-width: 1023px)  {
  .body {
    .description {
      padding-left: 2px;
      padding-right: 23px;
    }
  }
}
@media (max-width: 768px)  {
  .body {
    .links-and-btn {
      .tabs { 
        width: 55%;
      }
    }
  }
}
</style>