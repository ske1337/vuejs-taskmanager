<template>
  <div class="container">
    <h3>Add Task</h3>
    <input type="text" v-model="title"/>
    <button class="btn" @click="if(title.length)$emit('add-todo', title); (() => {title = ''})()">Add Task</button>
  </div>
</template>

<script>
export default {
  name: 'TodoAdd',
  data () {
    return {
      title: ''
    }
  }
}
</script>

<style scoped>
.container {
  padding: 10px;
  background-color: #eee;
  border-radius: 10px;
  margin: 30px auto 0 auto;
  width: 80%;
  max-width: 768px;
  display: flex;
  flex-direction: column;
}

.container input {
  padding: 3px;
  border: none;
  font-weight: 600;
}

.container .btn {
  margin-top: 10px;
  font-size: 1.1em;
  background-color: #afceff;
  border: none;
  border-radius: 15px;
  padding: 20px 0;
}

</style>
