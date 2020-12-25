<template>
  <div class="home">
    <div class="container">
      <div class="row header mb-5 p-3">
        <div class="col-lg-12">
          <h2>What I do Today</h2>
        </div>
      </div>

      <div class="row content">
        <div class="col-lg-12">
          <div class="pekerjaan-rumah">
            <div class="row">
              <div v-for="tugasSaya in tugas" v-bind:key="tugasSaya.id" class="mb-4 tugas col-lg-12 text-left">
                <div class="form-check">
                 <ItemTugas v-bind:tugasSaya="tugasSaya"></ItemTugas>
                </div>
            </div>
            </div>
          </div>
        </div>
      </div>

    </div>
    
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import "bootstrap/dist/css/bootstrap.css";
import ItemTugas from "../components/ItemTugas.vue";

export default {
  name: 'Home',
  data : function () {
    return {
      tugas : [
        {
            id : 0,
            namaTugas : "Membersihkan Halaman Rumah",
            isDone : false
        },
        {
            id : 1,
            namaTugas : "Memasak",
            isDone : false
        },
        {
            id : 2,
            namaTugas : "Ngoding dan Membaca",
            isDone : false
        }
      ]
    }
  },
  components: {
    ItemTugas
  }
}
</script>


<style scoped>
  .header {
    background: rgb(5, 156, 86);
  }

  .header h2 {
    margin: 0;
  }

  .tugas .item {
    font-size: 18px;
  }

  .item-compilated {
    color: rgb(5, 156, 86);
  }
</style>
