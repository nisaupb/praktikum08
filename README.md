# praktikum08
Buat program sederhana yang akan menampilkan daftar nilai mahasiswa, dengan ketentuan :

    Program dibuat dengan menggunakan Dictionary
    Tampilkan menu pilihan : (Tambah Data, Ubah Data, Hapus Data, Tampilkan Data, Cari Data)
    Nilai Akhir diambil dari perhitungan 3 komponen nilai (tugas : 30%, UTS : 35%, UAS : 35%)
    Buat flowchart dan penjelasan programnya pada README.md.
    Commit dan push repository ke github.

Langkah-langkah :

    Buat programnya terlebih dahulu seperti gambar di bawah ini

![image.png](screenshot/Screenshot%20(73).png)

print("====================================")
print("======>  Program Input Nilai  <======")
print("====================================")
data = {}
while True:
    print("")
    m = input("===>> (L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar : <=== ")
    print("================================================================")
    print("| NO |  Nama     |   Nim    |  Tugas  |  UTS  |  UAS  |   Akir |")
    print("================================================================")
    print(">>>>>>>>>>>>>>>>>>>>>>>> TIDAK ADA DATA <<<<<<<<<<<<<<<<<<<<<<<<")
    if m.lower() == 'k':
        break

    elif m.lower() == 'l':
        print("----- DAFTAR NILAI -----")
        print("==================================================================================")
        print("| NO |   NAMA     |   NIM        |  TUGAS   |   UTS     |   UAS      |  AKHIR    |")
        print("==================================================================================")
        i = 0
        for x in data.items():
            i += 1
            print("|  1 |{0:9}   |{1:9}     |{2:9} |{3:9}  |{4:9}   |{5:9}  |" .format(x[0], x[1][0],
                                                                                       x[1][1], x[1][2], x[1][3],
                                                                                       x[1][4], i))

        else:
            print("====================>>>>>>>>>>>>> Tidak Ada Data <<<<<<<<<<<<<====================")

    elif m.lower() == 't':
        print("--------------- Tambah Data ---------------")
        nama = input("Nama                  : ")
        nim = input("Nim                   : ")
        tugas = float(input("Masukan Nilai Tugas   : "))
        uts = float(input("Masukan Nilai UTS     : "))
        uas = float(input("Masukan Nilai UAS     : "))
        akhir = (int(tugas) * .30) + (int(uts) * .35) + (int(uas) * .35)
        data[nama] = nim, tugas, uts, uas, akhir

    elif m.lower() == 'u':
        print("----- Ubah Data Mahasiswa -----")
        nama = input("Nama  : ")
        if nama in data.keys():
            nim = input("Nim : ")
            tugas = float(input("masukan nilai tugas : "))
            uts = float(input("masukan nilai Uts : "))
            uas = float(input("masukan nilai uas : "))
            akhir = (int(tugas) * .30) + (int(uts) * .35) + (int(uas) * .35)
            data[nama] = nim, tugas, uts, uas, akhir

        else:
            print("Tidak Ada data")

    elif m.lower() == 'h':
        print("Hapus Data Mahasiswa")
        nama = input("nama : ")
        if nama in data.keys():
            print("Datanya", nama, "adalah {0}".format(data[nama]))
        else:
            print("Tidaak Ada Data")

    else:
        print("Pilih menu yang tersedia")

 
HASIL RUN = Tambah data ![image.png](screenshot/Screenshot%20(67).png)
            Lihat data  ![image.png](screenshot/Screenshot%20(68).png)
            Ubah data   ![image.png](screenshot/Screenshot%20(69).png)
            Hapus data  ![image.png](screenshot/Screenshot%20(70).png)
            cari data   ![image.png](screenshot/Screenshot%20(71).png)
            keluar      ![image.png](screenshot/Screenshot%20(72).png)


Penjelasan Program :

    Buatlah Dictionary berupa Nama, NIM, Nilai Tugas, Nilai UTS, Nilai UAS
    Lalu inputlah menu pilihan berupa Lihat, Tambah, Ubah, Hapus, Cari, Keluar
    Gunakanlah perulangan for, dengan perintah for i in range(len(Nama)):. Fungsi "len" ialah untuk mengembalikan panjang (jumlah anggota) dari suatu objek.
    Lalu inputlah Nama, NIM, Nilai Tugas, Nilai UTS, Nilai UAS
    Lalu mencari nilai akhir dengan perhitungan nilai tugas 30%, nilai uts 35% dan uas 35% , dengan perintah float
    Jika ingin melihat dictionary data ketik "L", jika ingin menambah data ketik "T", jika ingin mengubah data ketik "U", jika ingin menghapus ketik "H", jika ingin mencari data ketik "C" dan jika ingin keluar dari data ketik "K"
    Lalu cetak dengan perintah print ("Pilih menu yang tersedia")
    Selesai
