<template>
  <router-link
    class="patient-link"
    :to="{ name: 'PatientDetails', params: { id: patient.id } }"
  >
    <div class="patient-card">
      <span>Name: {{ patient.first_name }} {{ patient.last_name }}</span>
      <h4>{{ patient.vaccine_stat }}</h4>
    </div>
  </router-link>
</template>
<script>
export default {
  name: 'PatientCard',
  props: {
    patient: {
      type: Object,
      required: true
    }
  }
}
</script>
<style scoped>
.patient-card {
  padding: 20px;
  text-align: left;
  width: 97%;
  cursor: pointer;
  border: 1px solid #39495c;
  border-radius: 5px;
  margin-bottom: 18px;
}

.patient-card:hover {
  opacity: 100%;
  transform: scale(1.01);
  box-shadow: 0 3px 12px 0 rgba(0, 0, 0, 0.2);
}

.patient-link {
  color: #2c3e50;
  text-decoration: none;
}
</style>
