<template>
  <div id="talent-on-job">
    <!-- BREADCUMB -->
    <div class="d-flex align-items-center mb-3">
      <span class="fs-22">Manage Talents |</span>
      <i class="bi bi-person-fill-check mx-1 fs-14 mt-1"></i>
      <i class="bi bi-chevron-right fs-14 mt-1"></i>
      <small class="fs-14 mt-1">Talent o Job</small>
    </div>
    <!-- MAIN CONTENT -->
    <b-card>
      <b-card-header>
        <b-card-title class="d-flex align-items-center">
          Talent on Job
          <div class="ml-auto">
            <div class="input-group input-group-sm">
              <span class="input-group-text bg-white">
                <i class="bi bi-search fs-12"></i>
              </span>
              <input
                type="text"
                class="form-control form-talent"
                placeholder="Search..."
                v-model="data_table.filter"
              />
            </div>
          </div>
        </b-card-title>
        <span>Showing All of Talent on Job</span>
      </b-card-header>
      <b-card-body class="p-0 mt-3">
        <data_table striped hover :data="data_table"></data_table>
      </b-card-body>
    </b-card>
  </div>
</template>
<script>
import { BCard, BCardHeader, BCardBody, BTable } from "bootstrap-vue";
import data_table from "../../components/data_table.vue";

export default {
  name: "TalentOnJob",
  components: {
    BCard,
    BCardHeader,
    BCardBody,
    BTable,
    data_table,
  },
  data() {
    return {
      data_table: {
        row: 10,
        filter: "",
        fields: [
          {
            key: "no",
            label: "NO",
            thClass: "text-talent text-center ",
            tdClass: " text-talent text-center",
            thStyle: "background-color: #c1dbec;width:5%",
          },
          {
            key: "name",
            label: "NAME",
            thClass: "text-talent text-left ",
            tdClass: " text-talent text-left",
            thStyle: "background-color: #c1dbec;width:auto",
          },
          {
            key: "gender",
            label: "GENDER",
            thClass: "text-talent text-center ",
            tdClass: " text-talent text-center",
            thStyle: "background-color: #c1dbec;width:10%",
          },
          {
            key: "email",
            label: "EMAIL",
            thClass: "text-talent text-left ",
            tdClass: " text-talent text-left",
            thStyle: "background-color: #c1dbec;width:20%",
          },
          {
            key: "contact",
            label: "CONTACT",
            thClass: "text-talent text-center ",
            tdClass: " text-talent text-center",
            thStyle: "background-color: #c1dbec;width:5%",
          },
          {
            key: "status",
            label: "STATUS",
            thClass: "text-talent text-center ",
            tdClass: " text-talent text-center",
            thStyle: "background-color: #c1dbec;width:10%",
          },
          {
            key: "action",
            label: "NO",
            thClass: "text-talent text-center ",
            tdClass: " text-talent text-center",
            thStyle: "background-color: #c1dbec;width:15%",
          },
        ],
        items: [
          {
            id: 1,
            name: "Dickerson",
            gender: "Male",
            email: "Macdonald@gmail.com",
            status: "on_job",
          },
          {
            id: 2,
            name: "Larsen",
            gender: "Male",
            email: "Shaw@gmail.com",
            status: "free",
          },
          {
            gender: "Male",
            id: 3,
            name: "Geneva",
            email: "Wilson@gmail.com",
            status: "free",
          },
          {
            id: 4,
            name: "Jami",
            gender: "Female",
            email: "Carney@gmail.com",
            status: "on_job",
          },
          {
            id: 5,
            name: "Jami",
            gender: "Female",
            email: "Carney@gmail.com",
            status: "waiting",
          },
          {
            id: 6,
            name: "Jami",
            gender: "Male",
            email: "Carney@gmail.com",
            status: "waiting",
          },
          {
            id: 7,
            name: "Jami",
            gender: "Female",
            email: "Carney@gmail.com",
            status: "on_job",
          },
          {
            id: 8,
            name: "Jami",
            gender: "Male",
            email: "Carney@gmail.com",
            status: "on_job",
          },
          {
            id: 9,
            name: "Jami",
            gender: "Male",
            email: "Carney@gmail.com",
            status: "waiting",
          },
          {
            id: 10,
            name: "Jami",
            gender: "Male",
            email: "Carney@gmail.com",
            status: "on_job",
          },
          {
            id: 11,
            name: "Jami",
            gender: "Male",
            email: "Carney@gmail.com",
            status: "on_job",
          },
        ],
      },
    };
  },
};
</script>
