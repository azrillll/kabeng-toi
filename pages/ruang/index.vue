<template>
    <div class="container">
      <div class="content position-relative">
        <h2>Peminjaman Ruang</h2>
        <div class="form-group">
          <label>Nama Lengkap</label>
          <input type="text" class="form-control" v-model="namaLengkap">
        </div>
        <div class="form-group">
          <label>Jenis Kelamin</label>
          <select class="form-control" v-model="jenisKelamin">
            <option value="">Pilih Jenis Kelamin</option>
            <option value="Laki-laki">Laki-laki</option>
            <option value="Perempuan">Perempuan</option>
          </select>
        </div>
        <div class="form-group">
          <label>Tanggal</label>
          <input type="date" class="form-control" v-model="tanggal">
        </div>
        <div class="form-group">
          <label>Ruang yang mau di pinjam</label>
          <textarea class="form-control" v-model="ruang"></textarea>
        </div>
        <button class="btn btn-primary" @click="submitForm">Kirim</button>
        <button class="btn btn-primary position-absolute bottom-0 end-0" @click="navigateTo('/')">Kembali</button>
      </div>
    </div>
  </template>
  
  <script setup>
import { ref, onMounted } from 'vue'

  const useSupabaseClient = useSupabaseClient()
  const namaLengkap = ref("")
  const jenisKelamin = ref("")
  const tanggal = ref("")
  const ruang = ref("")
  
  async function submitForm() {
    const { error } = await supabase
    .from('ruang')
    .insert({ 
      namaLengkap: namaLengkap.value,
      jenisKelamin: jenisKelamin.value,
      tanggal: tanggal.value,
      ruang: ruang.value
     })
  }

  onMounted
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