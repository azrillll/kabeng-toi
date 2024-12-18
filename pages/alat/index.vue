<template>
  <div class="container">
    
      <div class="content position-relative rounded-5">
        <form @submit.prevent="submitForm">
        <h2>Peminjaman Alat</h2>
        <div class="form-group">
          <label>Nama Lengkap</label>
          <input type="text" class="form-control" v-model="form.namaLengkap">
        </div>
        <div class="form-group">
          <label>Jenis Kelamin</label>
          <select class="form-control" v-model="form.jenisKelamin" >
            <option value="Laki-laki">Laki-laki</option>
            <option value="Perempuan">Perempuan</option>
          </select>
        </div>
        <div class="form-group">
          <label>Tanggal</label>
          <input type="date" class="form-control" v-model="form.tanggal">
        </div>
        <div class="form-group">
          <label>Alat Yang Dipinjam</label>
          <textarea class="form-control" v-model="form.alat"></textarea>
        <button class="btn btn-primary" type="submit">Kirim</button>
        <nuxt-link to="/">
          <button class="btn btn-primary position-absolute bottom-0 end-0">Kembali</button>
        </nuxt-link>
        
      </div>
    </form>
    </div>
  
    </div>
  </template>
  
  <script setup>

// import { ref } from 'vue'; 
import { useRouter } from 'vue-router';

  const supabase = useSupabaseClient();
  const router = useRouter();

  const form = ref({
  tanggal: '',
  namaLengkap: '',
  jenisKelamin: '',
  alat: '',
})

const submitForm = async () => {
  console.log(form.value);
  const { error } = await supabase.from('alat').insert([form.value]);

  if (!error) {
    router.push('/');
  } else {
    console.error(error.message);
  }
}
  
  </script>
  
  <style scoped>
  .container {
    max-width: 800px;
    margin: 40px auto;
    padding: 20px;
    background-color: #f9f9f9;
    border: 1px solid #ddd;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  }
  
  .header {
    display: flex;
    align-items: center;
    margin-bottom: 20px;
  }
  
  .logo {
    width: 50px;
    height: 50px;
    margin-right: 10px;
  }
  
  h1 {
    font-size: 24px;
    font-weight: bold;
    margin-bottom: 10px;
  }
  
  p {
    font-size: 18px;
    color: #666;
  }
  
  .content {
    margin-top: 20px;
  }
  
  .form-group {
    margin-bottom: 20px;
  }
  
  label {
    display: block;
    margin-bottom: 10px;
  }
  
  input[type="text"], input[type="date"], select, textarea {
    width: 100%;
    height: 40px;
    padding: 10px;
    margin-bottom: 20px;
    border: 1px solid #ccc;
  }
  
  button[type="submit"] {
    background-color: #4CAF50;
    color: #fff;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }
  
  button[type="submit"]:hover {
    background-color: #3e8e41;
  }
  </style>

