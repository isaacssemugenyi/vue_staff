<template>
  <div class="container">
    <div class="row mt-3">
      <div class="col-md">
        <table class="table">
        <thead>
          <tr>
            <th scope="col">#</th>
            <th scope="col">Name</th>
            <th scope="col">Job</th>
            <th scope="col">Employed</th>
            <th>Change</th>
            <th>Remove</th>
          </tr>
        </thead>
          <tbody>
            <tr v-for="(staff, index) in staffs" :key="index" :style="jobStatus(staff)">
              <th scope="row">{{index + 1}}</th>
              <td>{{staff.name}}</td>
              <td>{{staff.title}}</td>
              <td>{{staff.isEmployed}}</td>
              <td><button @click="change(staff)" class="btn btn-primary"><span>&#8607;</span><span>&#8609;</span></button></td>
              <td><button @click="remove(index)" class="btn btn-warning">remove</button></td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  data(){
      return {
          staffs: [
              {name: 'Isaac Ssemugenyi', title: 'Developer', isEmployed: true},
              {name: 'Davies Wabuluka', title: 'Developer', isEmployed: false},
              {name: 'Eva Mirembe', title: 'Developer', isEmployed: true},
              {name: 'Sumaya Nabawanuka', title: 'Graphic Designer', isEmployed: true},
              {name: 'Queen Emilly Tusime', title: 'Lawyer', isEmployed: true},
              {name: 'Mugume Davies', title: 'Developer', isEmployed: false},
              {name: 'Phillip Jotham', title: 'Student', isEmployed: false},
              {name: 'Gridget Akankunda', title: 'Desginer', isEmployed: false},
              {name: 'Isaac Bazalaki', title: 'Developer', isEmployed: false}
          ]
      }
  },
  methods: {
    remove: function(index){
      this.staffs.splice(index, 1);
    },
    jobStatus: function(staff){
      if(!staff.isEmployed){
        return{
          color: 'red',
          'background-color': 'rgba(0,0,0,0.01)'
        }
      }
    },
    change: function(staff){
      return staff.isEmployed = !staff.isEmployed
    }
  }
}
</script>

<style scoped>
  
</style>
