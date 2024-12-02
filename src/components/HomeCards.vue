<script setup>
import Card from "./Card.vue"
</script>

<template>
  <section class="py-4">
    <div class="container-xl lg:container m-auto">
      <div class="grid grid-cols-1 md:grid-cols-2 gap-4 p-4 rounded-lg">
        <Card
          div-classes="bg-gray-100 p-6 rounded-lg shadow-md"
          title="For Developers"
          sub-title="Browse our Vue jobs and start your career today"
          btn-text="Browse Jobs"
          title-classes="text-2xl font-bold"
          sub-title-classes="mt-2 mb-4"
          btn-classes="inline-block bg-green-500 text-white rounded-lg px-4 py-2 hover:bg-green-600"
        />
        <Card
          div-classes="bg-green-100 p-6 rounded-lg shadow-md"
          title="For Employees"
          sub-title="List your jobs to find the perfect developer for the role"
          btn-text="Add Job"
          title-classes="text-2xl font-bold"
          sub-title-classes="mt-2 mb-4"
          btn-classes="inline-block bg-black text-white rounded-lg px-4 py-2 hover:bg-gray-700"
        />
      </div>
    </div>
  </section>
</template>
