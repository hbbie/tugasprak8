# tugasprak8
## Nama    :Dhani Naufal Habibie
## Kelas   :TI.24.A4
## NIM     : 312410300

## Dosen Pengampu: Agung Nugroho, S.Kom., M.Kom.
## Matkul  : Bahasa Pemrograman


# Latihan 1

![Screenshot 2024-12-09 074604](https://github.com/user-attachments/assets/fb8fa1a0-8546-42d8-b90f-c320a805495f)

```python
class DaftarNilaiMahasiswa:
    def __init__(self):
        """inisialisasi data mahasiswa"""
        self.data = {}

    def tambah(self, nama, nilai):
        """menambahkan data mahasiswa"""
        if nama in self.data:
            print(f"{nama} sudah ada. Gunakan metode 'ubah()' untuk memperbarui nilai.")
        else:
            self.data[nama] = nilai
            print(f"Data {nama} berhasil ditambahkan.")

    def tampilkan(self):
        """menampilkan semua data mahasiswa"""
        if not self.data:
            print("belum ada data yang dimasukkan.")
        else:
            print("\ndaftar Nilai Mahasiswa:")
            for nama, nilai in self.data.items():
                print(f"- {nama}: {nilai}")

    def hapus(self, nama):
        """menghapus data mahasiswa berdasarkan nama"""
        if nama in self.data:
            del self.data[nama]
            print(f"Data {nama} berhasil dihapus.")
        else:
            print(f"Data {nama} tidak ditemukan.")

    def ubah(self, nama, nilai_baru):
        """mengubah data mahasiswa berdasarkan nama"""
        if nama in self.data:
            self.data[nama] = nilai_baru
            print(f"Data {nama} berhasil diubah.")
        else:
            print(f"Data {nama} tidak ditemukan.")

if __name__ == "__main__":
    daftar = DaftarNilaiMahasiswa()

    while True:
        print("\nMenu:")
        print("1. Tambah Data")
        print("2. Tampilkan Data")
        print("3. Hapus Data")
        print("4. Ubah Data")
        print("5. Keluar")

        pilihan = input("Pilih menu (1-5): ")

        if pilihan == "1":
            nama = input("Masukkan nama: ")
            try:
                nilai = int(input("Masukkan nilai: "))
                daftar.tambah(nama, nilai)
            except ValueError:
                print("Nilai harus berupa angka!")
        elif pilihan == "2":
            daftar.tampilkan()
        elif pilihan == "3":
            nama = input("Masukkan nama yang akan dihapus: ")
            daftar.hapus(nama)
        elif pilihan == "4":
            nama = input("Masukkan nama yang akan diubah: ")
            try:
                nilai_baru = int(input("Masukkan nilai baru: "))
                daftar.ubah(nama, nilai_baru)
            except ValueError:
                print("Nilai harus berupa angka!")
        elif pilihan == "5":
            print("Program selesai. Terima kasih!")
            break
        else:
            print("Pilihan tidak valid. Silakan coba lagi.")
````

![Screenshot 2024-12-09 183648](https://github.com/user-attachments/assets/64b4e6e3-1b6a-46ba-9a24-3775d0e3233e)
![Screenshot 2024-12-09 183719](https://github.com/user-attachments/assets/f012b8ce-6712-46db-ac78-b299d7419b47)


Penjelasan program
# 1. Method tambah(nama, nilai)
Menambahkan data mahasiswa dengan nama sebagai key dan nilai sebagai value.

# 2. Method tampilkan()
Menampilkan seluruh data mahasiswa yang telah dimasukkan.

# 3. Method hapus(nama)
Menghapus data berdasarkan nama, jika nama ditemukan di dalam dictionary.
Fungsi: Menghapus data mahasiswa berdasarkan nama yang dimasukkan.  
- Penjelasan langkah-langkah:
  1. Meminta nama mahasiswa yang ingin dihapus.
  2. Mengecek apakah nama ada dalam dictionary:
     - Jika ada, menghapus data dengan `del`.
     - Jika tidak ada, menampilkan pesan bahwa data tidak ditemukan.
    
# 4. Method ubah(nama, nilai_baru)
Mengubah nilai mahasiswa berdasarkan nama, jika nama ditemukan di dalam dictionary.
Fungsi: Mengubah data mahasiswa yang sudah ada.  
- Penjelasan langkah-langkah:
  1. Meminta input nama mahasiswa.
  2. Mengecek apakah nama mahasiswa ada di dictionary.
  3. Jika nama ditemukan:
     - Meminta input nilai baru.
     - Memperbarui nilai mahasiswa di dictionary.
  4. Jika nama tidak ditemukan, menampilkan pesan bahwa data tidak ditemukan.

# Menu
```python
while True:
    ...
```
- Fungsi: Membuat menu interaktif untuk pengguna.  
- Penjelasan langkah-langkah:
  1. Menampilkan pilihan menu:
     - 1: Tambah data.
     - 2: Tampilkan data.
     - 3: Hapus data.
     - 4: Ubah data.
  2. Meminta input dari pengguna untuk memilih opsi menu.
  3. Berdasarkan pilihan:
     - Memanggil fungsi yang sesuai.
     - Jika pengguna memasukkan angka di luar 1-4, menampilkan pesan kesalahan.

# Hasil

![image](https://github.com/user-attachments/assets/c2d16078-7bee-4f8e-a482-41df00477eb0)


Terlihat bahwa saya menambahkan data mahasiswa yang bernama nopal 90 dan rapli 85

![image](https://github.com/user-attachments/assets/4042903f-fee7-485a-b47f-d8988535ecb5)


Saya meminta untuk menampilkan data mahasiswa yang saya masukan, karena saya hanya memasukan 2 data 2 mahasiswa bernama rapli dan nopal maka yang muncul akan itu

![image](https://github.com/user-attachments/assets/c1a2d983-8938-4312-9454-377344422f58)


Selanjutnya saya ingin mengubah nilai dari data rapli tersebut menjadi angka 100

![image](https://github.com/user-attachments/assets/1b64e18f-eba8-4640-8db5-bd9ba1d419b1)


Saya menghapus Data mahasiswa yang bernama nopal

#Flowchart

![flw](https://github.com/user-attachments/assets/5a65ef42-b39d-4d29-b993-418dab732686)
