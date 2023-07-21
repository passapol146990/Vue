<template>
    <div>
        <ul>
            <Person v-for="(item,index) in employee" 
            :key="index"
            :name="item.name"
            :salary="item.salary"
            :department="item.department"
            />
        </ul>
        <!-- <ul>
            เอาข้อมูลจาก App มาลง list แล้วส่งไป Person
            <Person v-for="(item,index) in employees" 
            :id="item.id"
            :key="index"
            :name="item.name"
            :salary="item.salary"
            :department="item.department"
            :isVisible="item.isVisible"
            @show="toggleVisible"
            @delete="removeEmployee"
            />
        </ul> -->
        <!-- <hr>
        เอาข้อมูลจาก list ไปแสดงใน person
        <Person name="พัสพล" salary=30000 />
        <Person name="บอย" salary=25000 />
        <Person name="เซฟ" salary=20000 /> -->
    </div>
</template>

<script>
import Person from './Person.vue'
export default { 
    name: "ListData",
    components: {
        Person,
    },
    props:["employee"],
    // ส่งข้อมูลไป person ถ้า App ส่งมาอันนี้ไม่ได้ใช้
    // data(){
    // return {
    //   employees:[
    //     {id:1, name:"พัสพล",salary:40000,department:"โปรแกรเมอร์",isVisible:false},
    //     {id:2, name:"บอย",salary:40000,department:"ขาย",isVisible:false},
    //     {id:3, name:"บอล",salary:40000,department:"ตลาด",isVisible:false},
    //     {id:4, name:"ไอคิว",salary:40000,department:"รับส่ง",isVisible:false},
    //     {id:5, name:"เกม",salary:40000,department:"ออกแบบ",isVisible:false},
    //     ]
    // }
    // },
    // methods:{
    //     toggleVisible(id){
    //         this.employees = this.employees.map((item)=>{
    //             if(item.id === id){
    //                 return {...item,isVisible:!item.isVisible}
    //             }
    //             return item
    //         })
    //     },
    //     removeEmployee(id){
    //         // filter เปรียบเทียมทั้งหมด
    //         this.employees = this.employees.filter(item=>{
    //             return item.id !== id
    //         })
    //     }
    // }
    // รับข้อมูลจากApp
    // props:["employees"]
}
</script>

<style>

</style>