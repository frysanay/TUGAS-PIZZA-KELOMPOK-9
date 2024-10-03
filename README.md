# TUGAS-PIZZA-KELOMPOK-9
ANGGOTA KELOMPOK:
Frysa Nayla Ayu(24091397162)
Ica Thalita Nartania(20491397158)
Ilham septian(24091397149)

# selamat datang di toko pizza antariksa
print(" selamat datang di toko pizza antariksa !")

# perintah untuk menghitung total biaya
def hitung_total_biaya(harga_pizza, tambahan_cheese):
    return harga_pizza + tambahan_cheese

# perintah pesanan pizza
def main():
    # daftar harga berdasarkan input yang diberikan
    harga_toping = {
        "pepperoni": 57000,
        "mushroom": 49000,
        "chicken": 56000,
        "vegetarian": 38000,
        "sausage": 30000,
        "paprica": 35000,
        "mozarella": 62000
    }
    
    harga_crust = {
        "thin": 12000,
        "thick": 18000,
        "cheese burst": 23000,
        "chilli cheesy stuffed": 37000,
        "stuffed": 33000
    }
    
    harga_ukuran = {
        "small": 49000,
        "medium": 78000,
        "large": 105000
    }
    
    tambahan_cheese = 13000  # biaya tambahan keju

    # input dari pengguna
    toping = input("masukkan toping pizza (pepperoni/mushroom/chicken/vegetarian/sausage/paprica/mozarella): ").lower()
    crust = input("masukkan crust pizza (thin/thick/cheese burst/chilli cheesy stuffed/stuffed): ").lower()
    ukuran = input("masukkan ukuran pizza (small/medium/large): ").lower()
    tambah_cheese = input("apakah anda ingin menambahkan keju? (yes/no): ").lower()

    # mengambil harga berdasarkan input pengguna
    harga_pizza = harga_toping.get(toping, 0) + harga_crust.get(crust, 0) + harga_ukuran.get(ukuran, 0)

    # jika pengguna ingin menambahkan keju, tambahkan biaya tambahan ke total
    if tambah_cheese == 'yes':
        harga_pizza = hitung_total_biaya(harga_pizza, tambahan_cheese)
    
    # output final
    print(f"Thank you for choosing Pizza Antariksa! Your final bill is: Rp. {harga_pizza}, pizza is waiting for you!")

# menjalankan perintah pesanan pizza
main()
