<script setup>
import TodoList from "./components/TodoList.vue";

const myTasks = [
  {title: 'Weed front garden.', completed: false},
  {title: 'Chill and smoke some Old Toby.', completed: false},
  {title: 'Keep ring secret and safe..', completed: true},
  {title: 'Meet Gandalf at Bree', completed: false},
  {title: 'Destroy ring and defeat dark lord', completed: false},
]
</script>

<template>
  <section class="mx-auto ">
    <h1 class="my-10 text-center">Components</h1>
    <div class="flex items-center justify-center h-[600px] font-medium">
      <div class="flex flex-grow items-center justify-center h-full text-gray-600 bg-gray-100">
        <!-- Component Start -->
        <TodoList title="Our Next Tasks" :tasks="myTasks" background="bg-white"/>
        <!-- Component End  -->
      </div>
      <TodoList  :tasks="myTasks"  background="bg-gray-800"  />
    </div>

  </section>
</template>


<style scoped>
input[type=checkbox]:checked + label span:first-of-type {
  background-color: #10B981;
  border-color: #10B981;
  color: #fff;
}

input[type=checkbox]:checked + label span:nth-of-type(2) {
  text-decoration: line-through;
  color: #9CA3AF;
}
</style>
