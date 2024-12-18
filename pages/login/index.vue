<template>
  <div>
    <h1>Sign Up</h1>

      <input v-model="email" type="email" placeholder="example@example.com" />
      <input v-model="password" type="password" placeholder="Password" />
    <button @click="handleSignup">Sign Up</button>
    <p v-if="error">{{ error }}</p>
  </div>
</template>

<script setup>
const supabase = useSupabaseClient()
async function addUser(email, password) {
  let { data, error } = await supabase
    .from('pengguna')  // Ganti dengan nama tabel Anda
    .insert([
      { email: email, password: password}  // Ganti dengan data yang ingin ditambahkan
    ]);

  if (error) {
    console.error('Error inserting data:', error);
  } else {
    console.log('Data inserted:', data);
  }
}
// Memanggil fungsi untuk menambahkan data
addUser('John Doe', 'johndoe@example.com');
</script>