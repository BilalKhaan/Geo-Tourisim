<template>
  <div class="categories">
    <div class="title">
      <span> Categories </span>
    </div>
    <div class="category-list">
      <div  v-for="(category, index) in categories" :key="index"
      class="category"
      :class="[index == 0 || index == 7 || index == 10 ? 'bg-blue' : 'bg-white']">
        <img src="@/assets/categories/biking-solid.svg" />
        <span> {{category.name}} </span>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data () {
    return {
      categories: [{
        id: 1, 
        name: "Architecture"
      }, {
        id: 2, 
        name: "Cycling"
      }, {
        id: 3, 
        name: "Driving"
      }, {
        id: 4, 
        name: "Educational"
      }, {
        id: 5, 
        name: "Food"
      }, {
        id: 6, 
        name: "Heritage"
      }, {
        id: 7, 
        name: "Nature"
      }, {
        id: 8, 
        name: "Shopping"
      }, {
        id: 9, 
        name: "Walking"
      }, {
        id: 10, 
        name: "For kids"
      }, {
        id: 11, 
        name: "Hotels"
      }, {
        id: 12, 
        name: "Trains"
      }, {
        id: 13, 
        name: "Described"
      }, {
        id: 14, 
        name: "Easter hunt"
      }, {
        id: 15, 
        name: "Arts & Culture"
      }, {
        id: 16, 
        name: "Entertainment"
      }, {
        id: 17, 
        name: "Life journey"
      }, {
        id: 18, 
        name: "Religious"
      }, {
        id: 19, 
        name: "Accessible"
      }, {
        id: 20, 
        name: "Haunted"
      }, {
        id: 21,
        name: "City tours"
      }, {
        id: 22,
        name: "Arts & Culture"
      }]
    }
  }
}
</script>
<style lang="scss" scoped>
.categories {
  margin-top: 72px;
  margin-bottom: 200px;
  .title {
    color: #373A3E;
    font-family: Avenir;
    font-size: 40px;
    font-weight: 900;
    letter-spacing: 0;
    line-height: 28px;
  }
  .category-list {
    margin-top: 35px;
    display: grid;
    grid-template-columns: 15% 15% 15% 15% 15% 15%;
    column-gap: 2%;
  }
  .category {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    border-radius: 8px;
    margin-bottom: 20px;
    box-shadow: 0 0 2px 0 rgba(0,0,0,0.05), 0 2px 2px 0 rgba(0,0,0,0.08), 0 0 8px 0 rgba(45,174,225,0.12), 0 8px 8px 0 rgba(45,174,225,0.24);
    img {
      width: 64px;
      height: 64px;
      padding: 10px 0px 7px 0px;
    }
    span {
      font-family: "Avenir";
      font-size: 14px;
      font-weight: 300;
      letter-spacing: 0;
      line-height: 19px;
      text-align: center;
      padding-bottom: 10px;
    }
  }
  .bg-white {
    background-color: white;
    color: #5B5C5E;
  }
  .bg-blue {
    background-color: #2DAEE1;
    color: #FFFFFF;
  }
}
@media  (min-width: 768px) and (max-width: 1023px)  {
  .categories {
    .category-list  {
      grid-template-columns: 24% 24% 24% 24%;
    }
  }
}
@media (max-width: 768px)  {
  .categories {
    .category-list  {
      grid-template-columns: 32% 32% 32% ;
    }
  }
}
</style>
