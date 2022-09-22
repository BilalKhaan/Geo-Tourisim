<template>
  <div class="left-portion">
    <div>
      <div class="heading">
        <span>Points</span>
      </div>
      <div class="count-points" v-for="(point, index) in points" :key="point.id">
        <div class="align-center">
          <div class="point-count">
            <span v-if="index != points.length - 1"> {{index + 1}} </span>
            <span v-else><img src="@/assets/images/Preview.png" /></span>
          </div>
          <div class="point-name">
            <span>{{ point.name }}</span>
          </div>
        </div>
      </div>
      <div class="heading" v-for="heading in headings" :key="heading.id">
        <span>{{ heading.name }}</span>
      </div>
    </div>  
  </div>
</template>

<script>
export default {
  data () {
   return {
     points: [{
       id: 1,
       name: 'Abbesses Metro Station'
     }, {
       id: 2,
       name: 'Pigalle and the Moulin R...'
     }, {
       id: 3,
       name: 'Create New'
     }],
     headings: [{
       id: 1,
       name: 'Media'
     }, {
       id: 2,
       name: 'Setting'
     }]
   }
  }
}
</script>
<style lang="scss" scoped>
.left-portion {
  width: 23%;
  border-top: 2px solid #2DAEE1;
  background: #F7F8F9;
  min-height: 67vh;
  padding-left: 25px;
  .heading {
    color: #373A3E;
    font-family: "Avenir";
    font-size: 20px;
    font-weight: 900;
    letter-spacing: 0;
    line-height: 28px;
    padding-top: 19px;
    padding-bottom: 17px;
    cursor: pointer;

  }
  .count-points {
    padding-top: 19px;
    padding-bottom: 17px;
    .point-count {
      box-sizing: border-box;
      height: 48px;
      width: 48px;
      border: 0.5px solid #D3DCE0;
      background-color: #FFFFFF;
      text-align: center;
      border-radius: 50%;
      span {
        color: #84898D;
        font-family: "Avenir";
        font-size: 20px;
        font-weight: 500;
        letter-spacing: 0;
        line-height: 26px;
        display: flex;
        justify-content: center;
        padding: 10px 0px;
      }
    }
    .point-name {
      margin-left: 30px;
      cursor: pointer;
      span {
        opacity: 0.7;
        color: #373A3E;
        font-family: "Avenir";
        font-size: 17px;
        font-weight: 500;
        letter-spacing: 0;
        line-height: 22px;
      }
    }
  }
}
@media  (min-width: 768px) and (max-width: 1023px)  {
  .left-portion {
    padding-left: 2px;
    .count-points  {
      .point-name {
        margin-left: 10px;
      }
    }
  }
}

</style>