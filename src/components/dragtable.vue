<template>
  <div style="padding:600px">
    <div id="drag-table">
      <table border="1" cellspacing="0">
        <tr>
          <th v-slldrag>id</th>
          <th v-slldrag>name</th>
          <th v-slldrag>old</th>
          <th v-slldrag>code</th>
          <th v-slldrag>level</th>
        </tr>
        <tr v-for="item of list">
          <td>{{item.id}}</td>
          <td>{{item.name}}</td>
          <td>{{item.old}}</td>
          <td>{{item.code}}</td>
          <td>{{item.level}}</td>
        </tr>
      </table>
    </div>
  </div>
</template>

<script>
  import Dragtable from "./dragtable";

  export default {
    name: 'dragtable',
    components: {Dragtable},
    data () {
      return {
        list:[
          {id:parseInt(Math.random()*10000000),name:'张三1',old:'11',code:'1ZS123456798',level:'主任1'},
          {id:parseInt(Math.random()*10000000),name:'张三2',old:'22',code:'2ZS123456798',level:'主任2'},
          {id:parseInt(Math.random()*10000000),name:'张三3',old:'33',code:'3ZS123456798',level:'主任3'},
          {id:parseInt(Math.random()*10000000),name:'张三4',old:'44',code:'4ZS123456798',level:'主任4'},
          {id:parseInt(Math.random()*10000000),name:'张三5',old:'55',code:'5ZS123456798',level:'主任5'},
          {id:parseInt(Math.random()*10000000),name:'张三6',old:'66',code:'6ZS123456798',level:'主任6'}
        ]
      }
    },
    methods:{ },
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  th,td{width:200px}
  #drag-table{
    position: relative;   /*定位*/
    -moz-user-select: none;
    -khtml-user-select: none;
    user-select: none;
  }

</style>
