<template>
  <header>
    <h1>ระบบจัดการข้อมูลพนักงาน</h1>
  </header>
  <Formconponent @save="insertEmployee" />
  <section v-if="employee.length>0">
    <h2 class="borderh2">ข้อมูลพนักงาน</h2>
    <ListData :employee="employee" class="employee-content" />
    <!-- <ListData class="employee-content" /> -->
  </section>
</template>


<script>
import ListData from './components/ListData.vue'
import Formconponent from './components/FormConponent.vue'
export default {
  name:"App",
  components:{
    ListData,
    Formconponent
},
  data(){
    return{
      employee:[],
    }
  },
  methods:{
    insertEmployee(data){
      this.employee.push(data);
    }
  },
  // ส่งข้อมูลไป list
  // <ListData :employee="employees" />
  // data(){
  //   return {
  //     employees:[
  //       {name:"พัสพล",salary:40000},
  //       {name:"บอย",salary:40000},
  //       {name:"บอล",salary:40000},
  //       {name:"ไอคิว",salary:40000},
  //       {name:"เกม",salary:40000},
  //       {name:"โจโจ้"}
  //     ]
  //   }
  // }
}
</script>



<style>
*{
  box-sizing: border-box;
}
body{
  margin: 0;
}
header{
  box-shadow: 0 2px 8px rgba(0,0,0,0.5);
  margin: 3rem;
  border-radius: 10px;
  padding: 1rem;
  background-color: orange;
  color: #fff;
}
.employee-content{
  box-shadow: 0 2px 8px rgba(0,0,0,0.5);
  margin: 3rem;
  border: 10px;
  padding: 1rem;
  border-radius: 20px;
}
.borderh2{
  border-radius: 10px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.5);
  margin: 3rem;
  margin-bottom: -2rem;
  padding: 1rem;
}
</style>