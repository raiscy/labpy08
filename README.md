# labpy08

# Praktikum 8

Buat program sederhana dengan mengaplikasikan penggunaan class. buatlah class untuk menampilkan daftar nilai mahasiswa, dengan ketentuan: 
1. Method tambah() untuk menambah data
2. Method tampilkan() untuk menampilkan data
3. Method hapus(nama) untuk menghapus data berdasarkan nama
4. Metode ubah(nama) untuk mengubah data berdasarkan nama 


        class Mahasiswa:
            def __init__(self):  # Perbaiki dari _init_ menjadi __init__
                self.data = {}

            def tambah(self, nama, nilai):
                self.data[nama] = nilai
                print(f"Data {nama} berhasil ditambahkan.")

            def tampilkan(self):
                if not self.data:
                    print("Belum ada data mahasiswa.")
                else:
                    print("Daftar Nilai Mahasiswa:")
                    for nama, nilai in self.data.items():
                        print(f"- Nama: {nama}, Nilai: {nilai}")

          def hapus(self, nama):
              if nama in self.data:
                  del self.data[nama]
                  print(f"Data {nama} berhasil dihapus.")
              else:
                  print(f"Data {nama} tidak ditemukan.")

        def ubah(self, nama, nilai_baru):
            if nama in self.data:
                self.data[nama] = nilai_baru
                print(f"Data {nama} berhasil diubah.")
            else:
                print(f"Data {nama} tidak ditemukan.")

        class Menu:
            def __init__(self):  # Perbaiki dari _init_ menjadi __init__
                  self.daftar = Mahasiswa()   

            def tampilkan_menu(self):
                print("\n===== Menu =====")
                print("1. Tambah Data")
                print("2. Tampilkan Data")
                print("3. Hapus Data")
                print("4. Ubah Data")
                 print("5. Keluar")
  
            def proses_input(self, menu):
                if menu == "1":
                    nama = input("Nama: ")
                    nilai = int(input("Nilai: "))
                    self.daftar.tambah(nama, nilai)
                elif menu == "2":
                    self.daftar.tampilkan()
                elif menu == "3":
                    nama = input("Nama: ")
                self.daftar.hapus(nama)
                    elif menu == "4":
                    nama = input("Nama: ")
                    nilai_baru = int(input("Nilai Baru: "))
                self.daftar.ubah(nama, nilai_baru)
                    elif menu == "5":
                    print("Terimakasih telah berkunjung.")
                        exit()
              else:
                    print("Pilihan tidak valid.")

        def jalankan(self):
        while True:
            self.tampilkan_menu()
            menu = input("Pilih menu (1-5): ")
            self.proses_input(menu)

        # Menjalankan aplikasi
             app = Menu()
              app.jalankan()

PROSES INPUT DATA 
![image](https://github.com/user-attachments/assets/a69ae3f7-ddde-4393-a391-dbf5e43461d6)
![image](https://github.com/user-attachments/assets/899576cd-5a4b-4ec7-ac22-3566ffe4499f)
![image](https://github.com/user-attachments/assets/c0668cb3-954f-498c-a9ac-b53f4581b2d9)

HASIL OUTPUT DATA 
![image](https://github.com/user-attachments/assets/2399a4c8-dbac-43c4-bdd1-18a041661e79)
![image](https://github.com/user-attachments/assets/96dc2312-1212-4886-bb71-24b657072d22)

PENJELASAN : 
1. Class 'Mahasiswa' berfungsi untuk menyimpan dan mengelola data mahasiswa. yang berisi : Atribut ('self.data') sebagai dictionary yang menyimpan nama mahasiswa dan nilai mahasiswa, Metode ('_ _ init_ _(self)'), ('tambah(self,nama,nilai)'),('tampilkan('self)'), ('ubah(self,nama,nilai_baru)'), dan ('hapus(self,nama)')
2. Class 'Menu' bertanggung jawab untuk menampilkan menu dan memproses input dari para pengguna, yang berisi : Atribut ('self.daftar') yang digunakan untuk mengakses metode yang ada di class 'Mahasiswa'.
3. Bagian akhir dari kode adalah menjalankannya.
4. Program sederhana ini adalah contoh dari penggunaan class dalam bahasa pemrograman python yang bertujuan untuk mengelola data.

FLOWCHART 

![flowchart](https://github.com/user-attachments/assets/f0cd216c-9650-428a-802d-cb8462697c01)

DIAGRAM CLASS

![DIAGRAM CLASS](https://github.com/user-attachments/assets/db7948d5-9d57-44f7-8a8b-943864928ffc)

