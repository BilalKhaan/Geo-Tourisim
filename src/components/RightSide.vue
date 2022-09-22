<template>
  <div class="right-portion"> 
    <div class="content">
      <div class="title">
        <span> Check List</span>
      </div>
      <div class="list flex-between" v-for="(check, index) in checkList" :key="index">
        <span :class="[index > 3 ? 'faded-name' : 'name']"> {{ check.name }}</span>
        <img src="@/assets/images/tick.png" />
      </div>
      <div class="buttons">
        <div class="preview button-common"> <span> Preview </span></div>
        <div class="publish button-common"> <span> Publish </span></div>
      </div>  
    </div>      
  </div>
</template>
<script>
export default {
  data () {
   return {
     checkList: [{
       id: 1,
       name: 'Name'
     }, {
       id: 2,
       name: 'Description'
     }, {
       id: 3,
       name: 'Cover Photo'
     }, {
       id: 4,
       name: 'At Least 1 pont'
     }, {
       id: 5,
       name: 'Narration'
     }, {
       id: 6,
       name: 'Category'
     }]
   }
  }
}
</script>
<style lang="scss" scoped>
.right-portion {
  width: 20%;
  display: flex;
  justify-content: space-between;
  .content {
    width: 85%;
    margin-top: 25px;
    box-sizing: border-box;
    border: 0.5px solid rgba(212,214,216,0.5);
    border-radius: 6px;
    background-color: #FFFFFF;
    box-shadow: 0 6px 12px 0 rgba(0,0,0,0.05);
    height: fit-content;
    .title {
      padding: 16px 0px 20px 20px;
      color: #373A3E;
      font-family: "Avenir";
      font-size: 20px;
      font-weight: 900;
      letter-spacing: 0;
      line-height: 28px;
    }
    .list {
      padding: 0px 15px 12px 21px;
      .name {
        color: #373A3E;
        font-family: "Avenir";
        font-size: 17px;
        font-weight: 500;
        letter-spacing: 0;
        line-height: 24px;
      }
      .faded-name {
        opacity: 0.6;
      }
      img {
        width: 22px;
        height: 22px;
      }
    }
  }
  .buttons {
    padding: 24px 17px 0px 17px;
    .preview {
      box-sizing: border-box;
      border: 1px solid #BCDEE8;
      border-radius: 32px;
      background-color: #F8FBFC;
      color: #2DAEE1;
    }
    .publish {
      border-radius: 32px;
      margin-top: 10px;
      margin-bottom: 18px;
      border: 1px solid #2DAEE1;
      background-color: #2DAEE1;
      box-shadow: 0 6px 9px 0 rgba(45,174,225,0.24);
      color: #FFFFFF;
    }
    .button-common {
      font-family: "Avenir";
      font-size: 18px;
      font-weight: 500;
      letter-spacing: 0;
      line-height: 20px;
      text-align: center;
      padding: 10px 0px;
      cursor: pointer;
      cursor: pointer;
    }
  }
}
</style>
