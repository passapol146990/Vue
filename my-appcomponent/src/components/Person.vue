<template>
  <Card>
    <template v-slot:card-header>
      <h2>{{ name }}</h2>
      <h4>เพศ: {{gender}}</h4>
      <p>เงินเดือน: {{salary}} บาท ตำแหน่งงาน: {{department}} ภาษาที่ถนัด:{{language}}</p>
    </template>
    <!-- <template v-slot:card-body>
      <button @click="ShowDescription(id)">ดูรายละเอียด</button>&nbsp;
      <button @click="DeleteEmployee(id)">ลบข้อมูล</button>
    </template> -->
    <!-- <template v-slot:card-footer>
      <transition name="fade">
        <div class="AddShow" v-show="isVisible">
          <p>salary: {{ salary }} บาท department: {{ department }}</p>
        </div>
      </transition>
    </template> -->
  </Card>
</template>

<script>
import Card from "./Card.vue";
export default {
  name: "PersonVue",
  components: {
    Card,
  },
  //รับค่าเข้ามาอย่างเดียว props:["name","salary"]
  //รับค่าและใส่ if else
  props: {
    // id: {
    //   type: Number,
    // },
    name: {
      type: String,
      //ต้องใส่ทุกครั้ง
      required: true,
    },
    salary: {
      type: Number,
      // กำหนดค่าเริ่มต้น
      default: 15000,
    },
    department: {
      type: String,
    },
    language:{
      type: String,
    }
    // isVisible: {
    //   type: Boolean,
    // },
  },
  // methods: {
  //   ShowDescription(id) {
  //     this.$emit("show", id);
  //   },
  //   DeleteEmployee(id) {
  //     this.$emit("delete", id);
  //   },
  // },
};
</script>

<style scoped>
h2 {
  color: black;
  margin-top: -20px;
}
/* ul {
  margin: 1rem 0;
  font-size: 1.25rem;
  font-weight: bold;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.3);
  padding: 0.5rem;
  color: #1f1f1f;
  border-radius: 25px;
} */
button {
  /* font: inherit; */
  cursor: pointer;
  border: 1px solid white;
  background: white;
  color: black;
  padding: 0.3rem 1rem;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.3);
  border-radius: 20px;
}
.fade-enter-from {
  opacity: 0;
}
.fade-enter-active {
  transition: all 0.5s linear;
}
button:hover {
  background: rgba(0, 0, 0, 0.3);
  border: 1px solid rgba(0, 0, 0, 0.3);
}
</style>