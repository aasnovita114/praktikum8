# praktikum8
Nama : AAS NOVITASARI

NIM : 312210167

Kelas : TI.22.A1


## Tugas Praktikum 8

Buat program sederhana dengan mengaplikasikan penggunaan class. Buatlah class untuk menampilkan daftar nilai mahasiswa, dengan ketentuan:


-Method tambah() untuk menambah data

-Method tampilkan() untuk menampilkan data

-Method hapus(nama) untuk menghapus data berdasarkan nama

-Method ubah(nama) untuk mengubah data berdasarkan nama

-Buat diagram class, flowchart dan penjelasan programnya pada README.md.

-Commit dan push repository ke github.

## Praktikum 8

## Rumus :

    class mahasiswa:

    def __init__(self, nim, nama, tugas, uts, uas):
        self.nim = nim
        self.nama = nama
        self.tugas = tugas
        self.uts = uts
        self.uas = uas

    def tambah(self,nim,nama,tugas,uts,uas):
        data.nim.append(nim)
        data.nama.append(nama)
        data.tugas.append(tugas)
        data.uts.append(uts)
        data.uas.append(uas)

    def lihat(self):
        for i in range(len(data.nama)):
            print("|", i+1, "  |", end="")
            print('{0:<25}'.format(self.nama[i]), end="")
            print("|", self.nim[i], end="")
            print(" |", self.tugas[i], end="")
            print("    |", self.uts[i], end="")
            print("  |", self.uas[i], " | ", end="")
            print(f'{((self.tugas[i]*30/100) + (self.uts[i]*35/100) + (self.uas[i]*35/100)) :.2f}', " |")

    def ubah(self,nim,nama,tugas,uts,uas):
        self.nim[no] = nim
        self.nama[no] = nama
        self.tugas[no] = tugas
        self.uts[no] = uts
        self.uas[no] = uas

    def hapus(self):
        del self.nim[no]
        del self.nama[no]
        del self.tugas[no]
        del self.uts[no]
        del self.uas[no]
        
    data = mahasiswa([],[],[],[],[])

    while True:

    menu = input("\n[(L)ihat, (T)ambah, (U)bah, (H)apus, (K)eluar]:")
    if menu == "t" or menu == "T":
    
       print("\nTambah Data")
       data.tambah(
           input("Masukkan NIM : "),
           input("Masukkan Nama : "),
           int(input("Nilai Tugas : ")),
           int(input("Nilai UTS : ")),
           int(input("Nilai UAS : "))
           )
       print("\nData berhasil ditambahkan")

    elif menu == "l" or menu == "L":
        print("\nDaftar Nilai")
        print("==========================================================================")
        print("| No  |          Nama           |    NIM    | TUGAS | UTS | UAS |  AKHIR |")
        print("==========================================================================")
        if len(data.nama) != 0:
            data.lihat()
        else:
            print("                         TIDAK ADA DATA                               ")
        print("==========================================================================")

    elif menu == "u" or menu == "U":
        print("\nUbah Data")
        ubah = input("Masukkan Nama : ")
        if ubah in data.nama:
           no = data.nama.index(ubah)
           print("Masukkan Data Yang Baru : ")
           data.ubah(
               input("NIM : "),
               input("Nama : "),
               int(input("Nilai Tugas : ")),
               int(input("Nilai UTS : ")),
               int(input("Nilai UAS : "))
               )
        else:
            print(ubah, "tidak ada di dalam data")

    elif menu == "h" or menu == "H":
        print("\nHapus Data")
        hapus = input("Masukkan Nama : ")
        if hapus in data.nama:
            no = data.nama.index(hapus)
            data.hapus()
            print("Data", hapus, "Berhasil dihapus")
        else:
            print(hapus, "tidak ada di dalam data")

    elif menu == "k" or menu == "K":
        print("\nTerimakasih\n")
        break

    else:
        print("\nPerintah yang dimasukkan salah!\n")
        
## Program :

![PRAKTIKUM8](https://user-images.githubusercontent.com/116045324/207204871-4f719f0d-f49f-43b4-88a9-bf1a0e31e398.PNG)

![PRAKTIKUM8-2](https://user-images.githubusercontent.com/116045324/207204919-dbcbc6f8-e631-41a9-99f3-e3dada17c0a3.PNG)


![PRAKTIKUM8-3](https://user-images.githubusercontent.com/116045324/207204961-f614b668-5894-4278-89a2-344cc134e53b.PNG)

![PRAKTIKUM8-4](https://user-images.githubusercontent.com/116045324/207205013-2df0fd29-6dde-4512-8d41-80ad34b5fff0.PNG)



## Hasil Run & Penjelasan Program:

-Pertama kita mendeklarasikan sebuah class mahasiswa yang didalamnya terdapat atribut NIM, Nama, nilai tugas, nilai UTS dan nilai UAS. Jangan lupa, untuk mendeklarasikan sebuah class didalam OOP kita harus menggunakan def__init__ dan juga self.

	class mahasiswa:
    def __init__(self, nim, nama, tugas, uts, uas):
        self.nim = nim
        self.nama = nama
        self.tugas = tugas
        self.uts = uts
        self.uas = uas
		
		
-Seperti biasa, deklarasikan satu dictionary kosong sebagai tempat menyimpan data-data yang sudah kita input. Ada 5 list kosong yang nantinya berisi NIM, Nama, nilai tugas, nilai UTS dan nilai UAS.

	data = mahasiswa([],[],[],[],[])  
	
-Kita akan buat beberapa method untuk menambahkan, menampilkan, menghapus, mengubah data mahasiswa. Pertama membuat method tambah(), method ini berfungsi untuk menambahkan data. Dalam method ini kita menggunakan append() supaya data yang terakhir ditambahkan ada di urutan list paling akhir.

	def tambah(self,nim,nama,tugas,uts,uas):
        data.nim.append(nim)
        data.nama.append(nama)
        data.tugas.append(tugas)
        data.uts.append(uts)
        data.uas.append(uas)
		
-Ini tampilan jika kita menginput	method :Tambah()
	

![HASILRUNPRAKTIKUM8](https://user-images.githubusercontent.com/116045324/207205136-4ffe14eb-d13a-4076-9736-f2a5e9c033b2.PNG)


-Fungsi membuat method lihat() yaitu untuk menampilkan seluruh data yang sudah kita tambahkan tadi. Jika tidak ada data sama sekali, maka akan muncul tulisan TIDAK ADA DATA.

	def lihat(self):
        for i in range(len(data.nama)):
            print("|", i+1, "  |", end="")
            print('{0:<25}'.format(self.nama[i]), end="")
            print("|", self.nim[i], end="")
            print(" |", self.tugas[i], end="")
            print("    |", self.uts[i], end="")
            print("  |", self.uas[i], " | ", end="")
            print(f'{((self.tugas[i]*30/100) + (self.uts[i]*35/100) + (self.uas[i]*35/100)) :.2f}', " |")
			
Ini tampilan jika kita menginput method : Lihat()

![HASILRUN2](https://user-images.githubusercontent.com/116045324/207205178-e40027d7-56fb-4e29-babe-c46da4d7b2e8.PNG)


-Fungsi membuat method ubah() yaitu untuk mengubah data. jika method ini diinput, maka data Nama, NIM, nilai tugas, nilai UTS, nilai UAS index nomor - (no) akan diubah sesuai dengan inputan dari user. Index ke - (no) akan dicari secara otomatis sesuai dengan nama yang ingin diubah oleh user.

	def ubah(self,nim,nama,tugas,uts,uas):
        self.nim[no] = nim
        self.nama[no] = nama
        self.tugas[no] = tugas
        self.uts[no] = uts
        self.uas[no] = uas
		
		
-Ini tampilan jika kita menginput method : Ubah()

![HASILRUN3](https://user-images.githubusercontent.com/116045324/207205246-08470d20-2242-48bc-8c9e-57608b7588e7.PNG)


![HASILRUN4](https://user-images.githubusercontent.com/116045324/207205291-e89452e4-c81f-4437-9c74-02ed3f5c90e2.PNG)


-Terakhir kita membuat method hapus(), yang berfungsi untuk menghapus data berdasarkan nama. Kita bisa menggunakan del untuk menghapus datanya. Seperti sebelumnya, nomor index list yang akan dihapus disesuaikan dengan inputan dari user. Yaitu index nomor ke - (no).

	def hapus(self):
        del self.nim[no]
        del self.nama[no]
        del self.tugas[no]
        del self.uts[no]
        del self.uas[no]
		
-Ini tampilan jika kita menginput method : Hapus()


![HASILRUN5](https://user-images.githubusercontent.com/116045324/207205339-e524cdfb-087b-4c44-9a4d-8053538e96c2.PNG)


## Diagram Class Praktikum 8


![image](https://user-images.githubusercontent.com/116045324/207205597-892ec790-4abd-4ebf-be44-047e71275a5b.png)



## Flowchart Praktikum 8


![image](https://user-images.githubusercontent.com/116045324/207205654-88755a04-a35c-49e0-baed-be6025c6c573.png)


## Sekian, Terima kasih
