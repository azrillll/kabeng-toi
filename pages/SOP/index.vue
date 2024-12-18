<template>
  <div class="container ">
    <div class="body">
      <div class="back-button">
        <i class="fas fa-arrow-left"></i>
      </div>
      <h1>SOP (Standar Oprating Procedure)</h1> 
      <div class="content">
        <form>
          <ol>
      
              <li>SOP (Standard Operating Procedure)</li>
              <li>Prosedur Operasi Standar / Tata Tertib Penggunaan laboratorium TOI SMKN 4 Tasikmalaya</li>
              <li>Waktu Operasional pukul 07.00 - 16.00 dan istirahat pukul 12.00 - 13.00 WIB</li>
              <li>Seluruh Siswa Laboratorium Komputer diwajibkan:</li>
            <li>Menggunakan seragam Praktik yang rapih selama Jadwal Praktik</li>
              <li>Mengisi Presensi Penggunaan Laboratorium TOI selama KBM (Kegiatan Belajar Mengajar) oleh Sekretaris Kelas/Guru Mapel</li>
              <li>Mencuci tangan dengan sabun sebelum masuk kedalam Laboratorium</li>
              <li>Melepas alas kaki dan memakai kaos kaki yang bersih atau dilepas</li>
              <li>Membersihkan Laboratorium sebelum dan sesudah digunakan</li>
              <li>Menjaga kebersihan dan merapikan laboratorium sebelum keluar ruangan</li>
              <li>Mengkonfirmasi terlebih dahulu ke Laboran/Kabeng sebelum memakai ruangan</li>
              <li>Merawat dan menjaga semua fasilitas didalam Laboratorium</li>
              <li>Mengisi form peminjaman alat/ruangan di https://kabengtoi.netlify.app</li>
              <li>Mengganti barang yang rusak sesuai jumlah dan spesifikasi alat yang rusak</li>
            <ul>
              <li>Seluruh Siswa Laboratorium TOI dilarang:</li>
                <li>Merangkap se ragam Praktik dengan seragam lain selama Jadwal Praktik (kecuali hari Senin)</li>
                <li>Membawa atau makan, minum dan merokok di Laboratorium</li>
                <li>Membuang sampah didalam Laboratorium dan toilet</li>
                <li>Membawa peralatan Laboratorium keluar ruangan Laboratorium tanpa izin Laobran</li>
                <li>Meninggalkan barang apapun milik pribadi tanpa seizin Laboran</li>
                <li>Meminjamkan alat selain untuk pembelajaran</li>
                <li>Menulis/menggambar di dinding, meja dan alat di Laboratorium</li>
                <li>Berisik, memutar musik/karaoke saat jam operasional</li>
                <li>Dilarang membawa orang luar Sekolah</li>
                <li>Dilarang membawa orang luar Jurusan (terkecuali izin kepada Laboran/Kabeng)</li>
                TTD
                Tasikmalaya, 1 Juli 2024
                Kepala Bengkel TOI,
                PAK ANA
                Last update: 2  2 November 2024
            </ul>
          </ol>
        </form>
        <div>
          <button class="btn btn-primary position-absolute bottom-0 end-0" @click="navigateTo('../')">Kembali</button>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
form {
  border: solid black 1px;
  width: 100%;
  padding: 10px 10px 10px 10px;
  background-color: grey;
}
li {
  color: black;
}
</style>