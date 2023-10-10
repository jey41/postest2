import os
from prettytable import PrettyTable
os.system('cls')

# Isi furniture yang dijual
furniture_items = [
    [1,"Lemari","Jati", "2500.000"],
    [2,"Meja belajar","Mahoni", "2500.000"],
    [3,"Kursi tammu","Jati", "800.000"],
    [4,"Meja makan","Gaharu", "2500.000"],
    [5,"Meja panjang","Jati", "2500.000"],
    ]

def tampilkan_furniture():
    table = PrettyTable()
    table.field_names = ["ID", " jenis Furniture", "Bahan", "Harga (Rp)"]
    
    for furniture in furniture_items:
        table.add_row(furniture)
    
    print(table)
    

def transaksi():
    while True:
        print("Daftar furniture yang tersedia")
        
        furniture_id = int(input("Masukkan ID furniture yang ingin dibeli: "))
        item_ditemukan = False
        for i in range(len(furniture_items)):
            if furniture_items[i][0] == furniture_id:
                nama_furniture = furniture_items[i][1]
                harga_furniture = furniture_items[i][3]
                print(f"Anda memilih untuk membeli furniture dengan id {furniture_id}: {nama_furniture} dengan harga {harga_furniture}.")
                break
            
        if not item_ditemukan:
            print(f"Tidak ada furniture dengan id: {furniture_id}")
        break
    
def menambahkan_furniture():
    print("=== Tambah Furniture ===")
    furniture_id = len(furniture_items) + 1
    name = input(" jenis Furniture: ")
    bahan = input("Bahan Furniture (ex: Jati, Mahoni,dll): ")
    price = str(input("Harga Furniture (Rp): "))
    furniture_items.append([furniture_id, name, bahan, price])
    
    print("Furniture telah ditambahkan!")

def update_furniture():
    while True:
        print("=== Perbarui Furniture ===")
        tampilkan_furniture()
        
        furniture_id = int(input("Masukkan ID Furniture yang akan diperbarui: "))
        item_ditemukan = False
        for i in range(len(furniture_items)):
            if furniture_items[i][0] == furniture_id:
                # Memasukan data yang baru
                jenis_item = input("Masukkan jenis furniture baru: ")
                bahan_item = input("Masukkan bahan furniture baru: ")
                harga_item = str(input("Masukkan harga furniture baru: "))
                
                # Melakukan update kepada data
                furniture_items[i][1] = jenis_item
                furniture_items[i][2] = bahan_item
                furniture_items[i][3] = harga_item
                
                print("Furniture telah diperbarui!")
                tampilkan_furniture()
                break
        if not item_ditemukan:
            print("Furniture dengan ID tersebut tidak ditemukan.")
        break


def menghapus_furniture():
    while True:
        print("=== Hapus Furniture ===")
        tampilkan_furniture()
        furniture_id = int(input("Masukkan ID item yang ingin dihapus: "))
        item_ditemukan = False
        for i in range(len(furniture_items)):
            if furniture_items[i][0] == furniture_id:
                # menghapus item sesuai input id
                furniture_items.pop(i)
                
                # menampilkan daftar item yang terbaru
                tampilkan_furniture()
                break
        if not item_ditemukan:
            print("Furniture dengan ID tersebut tidak ditemukan.")
        break
    
def menu_admin():
    while True:
        print("\nHai admin!!")
        print("Selamat datang di Toko Mabel Jepara!")
        print("1. Tampilkan furniture")
        print("2. Tambahkan furniture")
        print("3. Update furniture")
        print("4. Hapus furniture")
        print("0. Log out")
        
        operasi = (input("Pilih operasi? (0/1/2/3/4/): "))
        
        if operasi == "1":
            tampilkan_furniture()
        elif operasi == "2":
            menambahkan_furniture()
        elif operasi == "3":
            update_furniture()
        elif operasi == "4":
            menghapus_furniture()
        elif operasi == "0":
            print("Terimakasih sudah mampir!!")
            break
        else:
            print("Operasi yang anda masukan salah, coba lagi")
        

def menu_user():
    while True:
        print("\nHai user!!")
        print("Selamat datang di Toko Mabel Jepara!")
        print("1. Tampilkan furniture")
        print("0. Log out")
        
        operasi = (input("Pilih operasi? (0/1): "))
        
        if operasi == "1":
            tampilkan_furniture()
            transaksi()
        elif operasi == "0":
            print("\nTerimakasih sudah mampir!!")
            break
        else:
            print("Operasi yang anda masukan salah, coba lagi")


def tampilan_awal():
    while True:
        print("\nSelamat datang di Toko Mabel Jepara")
        print("1. Admin")
        print("2. User")
        print("3. Log out")
        role = input("Ingin masuk sebagai apa? (1/2/3): ")

        if role == "1":
            menu_admin()
        elif role == "2":
            menu_user()
        elif role == "3":
            print("Terimakasih sudah mampir!!")
            break
        else:
            print("Input salah, coba lagi")

if __name__ == "__main__":
    tampilan_awal()
