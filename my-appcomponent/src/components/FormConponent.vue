<template>
  <form @submit.prevent="submitForm">
    <h1>แบบฟอร์มบันทึกข้อมูล</h1>
    <div class="container">
      <div class="form-control">
        <label for="emp-name">ชื่อพนักงาน</label>
        <input type="text" v-model.trim="employees.name" />
      </div>
      <div class="form-control">
        <label for="emp-salary">เงินเดือนพนักงาน</label>
        <input type="Number" v-model="employees.salary" />
      </div>
      <div class="form-control">
        <h2 for="department">ตำแหน่งงาน</h2>
        <select v-model="employees.department">
          <option value="ฝ่ายการตลาด">ฝ่ายการตลาด</option>
          <option value="ฝ่ายขาย">ฝ่ายขาย</option>
          <option value="ฝ่ายออกแบบ">ฝ่ายออกแบบ</option>
        </select>
      </div>
      <div class="">
        <h2>เพศ</h2>
        <div>
          <input type="radio" value="ชาย" v-model="employees.gender">
          <label for="gender-name">ชาย</label>
        </div>
        <div>
          <input type="radio" value="หญิง" v-model="employees.gender">
          <label for="gender-name">หญิง</label>
        </div>
      </div>
      <div class="">
        <h2>ภาษาที่ถนัด</h2>
        <div>
          <input type="checkbox" value="html" v-model="employees.language">
          <label for="html">HTML</label>
        </div>
        <div>
          <input type="checkbox" value="Java" v-model="employees.language">
          <label for="html">Java</label>
        </div>
        <div>
          <input type="checkbox" value="python" v-model="employees.language">
          <label for="html">python</label>
        </div>
      </div>
      <div class="mt-2">
        <button >บันทึกข้อมูล</button>
      </div>
    </div>
    <!-- ดูค่าข้อมูล -->
    <!-- {{ JSON.stringify(employees) }} -->
  </form> 
</template>

<script>
export default {
  name: "FormComponent",
  data() {
    return {
      employees: {
        name: "",
        salary: "",
        department: "ฝ่ายการตลาด",
        gender: "",
        language: [],
      },
    };
  },  
  methods:{
    submitForm(){
      const newEmployee={
        name:this.employees.name,
        salary:this.employees.salary,
        department:this.employees.department,
        gender:this.employees.gender,
        language:this.employees.language,
      }
      // ส่งให้App
      this.$emit("save",newEmployee);
    }
  }
};
</script>

<style scoped>
form {
  margin: 2rem auto;
  max-width: 40rem;
  border-radius: 15px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.25);
}
.container {
  margin-top: -3rem;
  padding: 2rem;
}
h1 {
  padding: 2%;
}
.form-control input {
  display: block;
  width: 100%;
  height: 2rem;
  margin-bottom: 10px;
}
button,
select {
  height: 2rem;
  width: 9rem;
  border-radius: 5px;
  border: 1px solid rgba(0, 0, 0, 0.25);
  background: #fff;
}
.mt-2{
  margin-top: 2rem;
}
button:hover {
  height: 2rem;
  width: 9rem;
  border-radius: 5px;
  border: 1px solid rgba(0, 0, 0, 1);
  background: green;
  color: #fff;
}
input[type="radio"],input[type="checkbox"] {
  display: inline-block;
  width: auto;
  margin-right: 1rem;
}
input[type="radio"] + label ,input[type="checkbox"]+label{
  font-weight: normal;
}
h2 {
  font-size: 1rem;
  margin: 0.5rem 0;
}
</style>