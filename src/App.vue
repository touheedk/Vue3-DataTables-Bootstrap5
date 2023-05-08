<script setup lang="ts">
import DataTable from 'datatables.net-vue3';
import DataTablesCore from 'datatables.net-bs5';

DataTable.use(DataTablesCore);
const data = [
  {
    id: '1',
    name: 'Touheed Khan',
    position: 'Senior Developer',
    salary: '$320,800',
    office: 'Mumbai',
  },
  {
    id: '2',
    name: 'Alex Max',
    position: 'Manger',
    salary: '$470,750',
    office: 'Paris',
  },
  {
    id: '3',
    name: 'Amar Arjun',
    position: 'Technical Author',
    salary: '$286,000',
    office: 'Berlin',
  },
];

const columns = [
  { data: 'name' },
  { data: 'position' },
  { data: 'office' },
  { data: 'salary' },
];
</script>

<template>
  <div class="container">
    <h2>Employee List</h2>
    <DataTable
      :columns="columns"
      :data="data"
      class="table table-hover table-striped"
      width="100%"
    >
      <thead>
        <tr>
          <th>Name</th>
          <th>Position</th>
          <th>Office</th>
          <th>Salary</th>
        </tr>
      </thead>
    </DataTable>
  </div>
</template>

<style>
@import 'bootstrap';
@import 'datatables.net-bs5';
</style>
