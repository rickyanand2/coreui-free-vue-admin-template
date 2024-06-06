<template>
    <CCard>
      <CCardHeader>
        <strong>Scan List</strong>
      </CCardHeader>
      <CCardBody>
        <!-- Add your table or list component here to display the scans -->
        <CDataTable
          :items="scans"
          :fields="fields"
          hover
          striped
          bordered
          items-per-page="5"
          pagination
        />
      </CCardBody>
    </CCard>
  </template>
  
  <script setup>
  import { ref } from 'vue'
  import { CCard, CCardHeader, CCardBody, CDataTable } from '@coreui/vue'
  
  const scans = ref([
    { id: 1, name: 'Scan 1', date: '2023-06-01' },
    { id: 2, name: 'Scan 2', date: '2023-06-02' },
  ])
  
  const fields = ref([
    { key: 'id', label: 'ID' },
    { key: 'name', label: 'Name' },
    { key: 'date', label: 'Date' },
  ])
  </script>
  