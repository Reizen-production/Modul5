# Modul5
1. Buatlah menu sebagai basic perintah untuk Tambah,Lihat,Ubah,Hapus,Cari,Keluar sperti berikut:
- perintah = input("(T)ambah, (L)ihat, (U)bah, (H)apus, (C)ari, (K)eluar: ")

2. Untuk menambahkan data, gunakan
- if perintah.lower() == 't':
- nim = input("Masukan NIM: ")
- nama = input("Masukan nama: ")
- n_tugas = int(input("Masukan nilai tugas: "))
- n_UTS = int(input("Masukan nilai UTS: "))
- n_UAS = int(input("Masukan nilai UAS: "))
- a = n_tugas * 30 / 100
- b = n_UTS * 35 / 100
- c = n_UAS * 35 / 100
- n_akhir = a + b + c
- daftar[nama] = [nama, nim, n_tugas, n_UTS, n_UAS, n_akhir]
- jangan lupa gunakan nested dictionary dalam menambahkan data

3.untuk metode print, dapat digunakan sebagai berikut : 
- elif perintah.lower() == 'l':
- print("Daftar Nilai:")
- print("===================================================================")
- print("| No |      Nama      |    NIM    | Tugas |  UTS  |  UAS  | Akhir |")
- print("===================================================================")
- no = 1
-        for tabel in daftar.values():
-            print("| {0:2} | {1:14} | {2:9} | {3:5} | {4:5} | {5:5} | {6:5} |".format
-                  (no, tabel[0],
-                   tabel[1], tabel[2],
-                   tabel[3], tabel[4], tabel[5]))
-            no += 1
-
4. untuk ubah data dimasukan syntax seperti berikut : 
-    elif perintah.lower() == 'u':
-        nama = input("Masukan nama untuk mengubah data: ")
-        if nama in daftar.keys():
-            print("Masukan data yang ingin di ubah :")
-            data = input("(Semua), (Nama), (NIM), "
-                         "(Tugas), (UTS), (UAS) : ")
-            if data.lower() == "semua":
-                print("==========================")
-                print("Ubah data {}.".format(nama))
-                print("==========================")
-                daftar[nama][1] = input("Edit NIM:")
-                daftar[nama][2] = int(input("Edit Nilai Tugas: "))
-                daftar[nama][3] = int(input("Edit Nilai UTS: "))
-                daftar[nama][4] = int(input("Edit Nilai UAS: "))
-                # print(daftar)
-            elif data.lower() == "nim":
-                daftar[nama][1] = input("NIM:")
-            elif data.lower() == "tugas":
-                daftar[nama][2] = int(input("Nilai Tugas: "))
-            elif data.lower() == "uts":
-                daftar[nama][3] = int(input("Nilai UTS: "))
-            elif data.lower() == "uas":
-                daftar[nama][4] = int(input("Nilai UAS: "))
-            else:
-                print("Perintah tidak ditemukan.")

-        else:
-            print("'{}' tidak ditemukan.".format(nama))

5. Untuk mencari data gunakan :

-    elif perintah.lower() == 'c':
-        print("Mencari daftar nilai: ")
-        print("=================================================")
-        nama = input("Masukan nama untuk mencari daftar nilai : ")
-        if nama in daftar.keys():
-            print("Nama {0}, dengan NIM : {1}\n"
-                  "Nilai Tugas: {2}, UTS: {3}, dan UAS: {4}\n"
-                  "dan nilai akhir {5}".format(nama, daftar[nama][1],
-                                               daftar[nama][2], daftar[nama][3],
-                                               daftar[nama][4], daftar[nama][5]))
-        else:
-            print("'{}' tidak ditemukan.".format(nama))

6. Dan hapus data :
-    elif perintah.lower() == 'h':
-        nama = input("Masukan nama untuk menghapus data : ")
-        if nama in daftar.keys():
-            del daftar[nama]
-            print("Data '{}' dihapus.".format(nama))
-        else:
-            print("'{}' tidak ditemukan.".format(nama))

7. dan untuk keluar dari menu cukup mudah dan bersifat umum: 
-    elif perintah.lower() == 'k':
-        break

 -   else:
 -       print("Silahkan masukan perintah terlebih dahulu.")
