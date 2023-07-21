<template>
  <section>
    <button @click="ToggleisVisible3">{{isVisible ? "ซ่อน":"แสดง"}}รายละเอียด</button>
    คำนวณเกรด
    <article v-show="isVisible3">
      <form @submit.prevent="gradecal">
        ใส่เกรดของท่าน : <input type="text" ref="Grade" placeholder="Grade">
        <button>ok</button>
        <label> ท่านได้เกรด: {{grade}}</label>
      </form>
    </article>
    <br>
    <button @click="ToggleisVisible">{{isVisible ? "ซ่อน":"แสดง"}}รายละเอียด</button>
    ดึง Array ด้วย v-for
    <article v-show="isVisible">
      ดึง Array ด้วย v-for
      <ul>
        <li v-for="(item,index) in grade1" :key="index">{{index}} {{item}}</li>
      </ul>
      <hr>
      ดึง Array key ด้วย v-for
      <ul>
        <li v-for="(color1,key) in color" :key="key">{{key}} = {{color1}}</li>
      </ul>
    </article>
    <br>
    <button @click="ToggleisVisible1">{{isVisible1 ? "ซ่อน":"แสดง"}}รายละเอียด</button>
    รูป ชื่อ ลิ้งก์ ul button
    <article v-show="isVisible1">
      <img :src="image" :width="size" :height="size"/>
      <h1>long name : {{fname}}</h1>
      <h1>name : {{name}}</h1>
      <h1>age :{{age}}</h1>
      <p>ที่อยู่:<span v-html="address"></span></p>
      <a :href="anime" target="_black">Anime</a>
      <p>friend</p>
      <ul>
        <li>{{friend[0]}}</li>
        <li>{{friend[1]}}</li>
        <li>{{friend[2]}}</li>
      </ul>
      <ul>
        <li>{{color.g}}</li>
        <li>{{color.r}}</li>
        <li>{{color.y}}</li>
      </ul>
      <button v-on:click="ShowData">v-on Showdata</button>
      <button @click="ShowData">@ShowData</button>
      <!-- <button @click="addage">+1 age</button>
      <button @click="reduce">-1 age</button> -->

      <button @click="addage(10)">+10 age</button>
      <button @click="reduce(10)">-10 age</button>
      <br>
    </article>
    <br>
    <button @click="ToggleisVisible2">{{isVisible2 ? "ซ่อน":"แสดง"}}รายละเอียด</button>
    Input text
    <article v-show="isVisible2">
      ป้อนชื่อเล่น : <input type="text" v-on:input="setFname">
      <br>
      <h2>{{Fname}}</h2>
      <hr>
      บันทึกข้อมูล
      <form @submit.prevent="submitForm">
        <input type="text" v-on:input="setFname" placeholder="ใส่ข้อความที่ต้องการ">
        <button>ok</button>
      </form>
      <hr>
      กดเพื่อบันทึกข้อมูล
      <form @submit.prevent="submitForm2">
        <input type="text" ref="inputform2">
        <p>{{NamesubmitForm2}}</p>
        <button>ok</button>
      </form>
    </article>
    <br>
    <button @click="ToggleisVisible4">{{isVisible4 ? "ซ่อน":"แสดง"}}รายละเอียด</button>
    random and methods and computed
    <article v-show="isVisible4">
      <h2>{{getrandom()}}</h2>
      <h2>{{getrandom()}}</h2>
      <hr>
      <h2>{{getrandom1}}</h2>
      <h2>{{getrandom1}}</h2>
    </article>
  </section>
</template>

<script>
export default {
  name: 'App',
  data(){
    return{
      isVisible: false,
      isVisible1: false,
      isVisible2: false,
      isVisible3: false,
      isVisible4: false,
      grade:"",
      grade0:"",
      grade1:['A','B','C','D','E','F'],
      fname:'พล',
      Fname:"ข้อความจะแสดงตรงนี้",
      name:'พัสพล สุทาธรรม',
      age:18,
      address:'<i>กรุงเทพ</i>',
      image:'https://animekimi.com/wp-content/uploads/2022/07/dfGf0Ti3BEKpBpVCVtEXKTjQjNR-185x278.jpg',
      size:150,
      anime:'https://animekimi.com/anime/lycoris-recoil/',
      friend:['phol','boy','saf'],
      color:{g:'green',r:'red',y:'yellow'},
      NamesubmitForm2: "",
    }
  },
  methods:{
    gradecal(){
      this.grade0 = this.$refs.Grade.value
      if(this.grade0 > 100 || this.grade0 < 0){
        this.grade = "Error"
      }else{
        if(this.grade0 >= 80 & this.grade0 <= 100){ this.grade = 'A'}
        if(this.grade0 >= 70 & this.grade0 <= 79){ this.grade = 'B'}
        if(this.grade0 >= 60 & this.grade0 <= 69){ this.grade = 'C'}
        if(this.grade0 >= 50 & this.grade0 <= 59){ this.grade = 'D'}
        if(this.grade0 >= 0 & this.grade0 <= 49){ this.grade = 'F'}
      }
    },
    getFullname(){
      return `${this.fname} ${this.name}`
    },
    ShowData(){
      alert(this.getFullname())
    },
    addage(value){
      this.age+=value
    },
    reduce(value){
      this.age-=value
    },
    setFname(event){
      this.Fname = event.target.value
    },
    submitForm(){
      alert("บันทึกข้อมูลเรียบร้อยแล้ว")
    },
    submitForm2(){
      this.NamesubmitForm2 = this.$refs.inputform2.value
    },
    ToggleisVisible(){
      this.isVisible = !this.isVisible
    },
    ToggleisVisible1(){
      this.isVisible1 = !this.isVisible1
    },
    ToggleisVisible2(){
      this.isVisible2 = !this.isVisible2
    },
    ToggleisVisible3(){
      this.isVisible3 = !this.isVisible3
    },
    ToggleisVisible4(){
      this.isVisible4 = !this.isVisible4
    },
    getrandom(){
      return Math.random()
    },
  },
  computed:{
    getrandom1(){
      return Math.random();
    },
  }
};
</script>

<style>
</style>
