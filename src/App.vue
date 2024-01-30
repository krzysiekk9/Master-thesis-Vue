<script>
import Header from './components/Header.vue'
import Row from './components/Row.vue'
import Img from './components/Img.vue'

export default{
  data(){
    return {
      rowNum: 0,
      imgNum: 0,
      arr: [],
      arr2: [1],
    }
  },
  components:{
    Header,
    Row,
    Img
  },
  methods: {
    // Metody dotyczące tabel
    create(amount){
      this.rowNum = amount;
      this.createTable(this.rowNum)
    },
    add(amount){
      this.rowNum = this.rowNum + amount;
      this.createTable(this.rowNum);
    },
    deleteTab(){
      this.rowNum = 0;
      this.arr = [];
    },
    createTable(count, array=this.arr){
      for (let i = 1; i <= count; i++) {
        array[i] = i;
      }
    },
    //metody dotyczące zdjęć
    createImg(amount) {
      this.imgNum = amount;
      for (let i = 1; i < this.imgNum; i++) {
        this.arr2[i] = i;
      }
    },
    deleteImg(){
      this.arr2 = [1]
    }
  }
}
</script>

<template>
  <Header v-bind="{create, add, deleteTab, createImg, deleteImg}"/>
  <table class="table">
    <tbody>
      <Row 
        v-for="element in arr"
        :rowNum="element" 
      />
    </tbody>
  </table>
  <Img v-for="element in arr2"
    v-bind="{element}" 
  />
</template>

