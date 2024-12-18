<template>
  <div class="container-fluid">
      <div class="row">
          <div class="col-lg-12">
              <h2 class="text-center my-4">riwayat peminjaman alat</h2>
              <div class="my-3">
                  <form @submit.prevent="getPeminjaman">
                      <input v-model="keyword" type="search" class="form-control rounded-5" placeholder="Filter...">
                  </form>
              </div>
              <div class="my-3 text-muted">menampilkan daftar riwayat</div>
              <table class="table table-bordered">
                  <thead>
                      <tr>
                          <td>No</td>
                          <td>Nama</td>
                          <td>Tanggal peminjaman</td>
                          <td>Alat yg dipinjam</td>
                      </tr>
                  </thead>
                  <tbody>
                      <tr v-for="(user, i) in users" :key="i">
                          <td>{{ i + 1 }}.</td>
                          <td>{{ user.nama }}</td>
                          <td>{{ user.tanggal_peminjaman }}</td>
                          <td>{{ user.alat }}</td>
                      </tr>
                  </tbody>
              </table>
          </div>
      </div>
      <NuxtLink to="../">
          <button type="submit" class="btn btn-dark btn-lg rounded-5 px-5">kembali</button>
      </NuxtLink>
  </div>
</template>
<script setup>
const supabase = useSupabaseClient()
const keyword = ref('')
const user = ref([])

const getRiwayat = async () => {
  const { data, error } = await supabase.from('riwayat').select(`*, alat(*)`).order('id', { ascending: false })
  if (data) user.value = data
}

onMounted(() => {
  getRiwayat()
})
</script>