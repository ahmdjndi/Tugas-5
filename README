STUDI KASUS 1

import java.util.Scanner; = mengimpor kelas Scanner untuk membaca input dari pengguna

class Mahasiswa { = mendefinisikan sebuah kelas bernama Mahasiswa
String nim; = deklarasi atribut dari kelas nim bertipe String
String nama; = deklarasi atribut dari kelas nama bertipe String
String jurusan; = deklarasi atribut dari kelas jurusan bertipe String
double ipk; = atribut ipk (Indeks Prestasi Kumulatif) yang bertipe double

public Mahasiswa(String nim, String nama, String jurusan, double ipk) { = konstruktor dari kelas Mahasiswa digunakan untuk mengisi nilai atribut
this.nim = nim; = mengisi nilai atribut nim dengan nilai yang diberikan
this.nama = nama; = mengisi atribut nama dengan nilai dari parameter nama
this.jurusan = jurusan; = mengisi atribut jurusan dengan nilai dari parameter jurusan
this.ipk = ipk; = mengisi atribut ipk dengan nilai dari parameter ipk
} = penutup untuk konstruktor 

@Override = anotasi yang memberi tahu compiler bahwa metode di bawahnya akan meng-override metode yang ada di superclass-nya
public String toString() { = deklarasi metode toString(), yang bertipe String dan bersifat public
return String.format("NIM: %s\nNama: %s\nJurusan: %s\nIPK: %.2f", nim, nama, jurusan, ipk); = mengembalikan sebuah String hasil dari String.format(), yang membuat teks terformat rapi dengan menyisipkan nilai-nilai atribut nim, nama, jurusan, dan ipk
} = penutup untuk metode toString()
} = penutup untuk kelas Mahasiswa

public class Studi_kasus_1 { = mendeklarasikan kelas publik bernama Studi_kasus_1
public static void main(String[] args) { = main method
// Data mahasiswa 
Mahasiswa[] daftarMahasiswa = { = membuat array berisi objek-objek Mahasiswa. Nama variabelnya adalah daftarMahasiswa
new Mahasiswa("2023001", "Budi Santoso", "Teknik Informatika", 3.75), = membuat objek mahasiswa dengan "2023001", "Budi Santoso", "Teknik Informatika", 3.75
new Mahasiswa("2023002", "Andi Wijaya", "Sistem Informasi", 3.50), = membuat objek mahasiswa dengan "2023002", "Andi Wijaya", "Sistem Informasi", 3.50
new Mahasiswa("2023003", "Dewi Lestari", "Teknik Komputer", 3.90), = membuat objek mahasiswa dengan "2023003", "Dewi Lestari", "Teknik Komputer", 3.90
new Mahasiswa("2023004", "Rina Maulana", "Teknik Informatika", 3.60), = membuat objek mahasiwa dengan "2023004", "Rina Maulana", "Teknik Informatika", 3.60
new Mahasiswa("2023005", "Doni Kusuma", "Manajemen Informatika", 3.25), = menbuat objek mahasiswa dengan "2023005", "Doni Kusuma", "Manajemen Informatika", 3.25
new Mahasiswa("2023006", "Sinta Rahma", "Sistem Informasi", 3.85), = membuat objek mahasiswa dengan"2023006", "Sinta Rahma", "Sistem Informasi", 3.85
new Mahasiswa("2023007", "Rudi Hermawan", "Teknik Komputer", 3.40) = membuat objek mahasiswa dengan "2023007", "Rudi Hermawan", "Teknik Komputer", 3.40
};

Scanner scanner = new Scanner(System.in); = membuat objek Scanner untuk membaca input dari pengguna

System.out.println("=== SISTEM PENCARIAN DATA MAHASISWA ==="); = menampilkan judul "SISTEM PENCARIAN DATA MAHASISWA"
System.out.print("Masukkan NIM Mahasiswa yang dicari: "); = menampilkan prompt kepada pengguna untuk memasukkan NIM.
String nimCari = scanner.nextLine(); = membaca input NIM dari pengguna dan menyimpannya dalam variabel nimCari

// Lakukan pencarian linear
Mahasiswa hasilPencarian = cariMahasiswaByNIM(daftarMahasiswa, nimCari); = memanggil metode cariMahasiswaByNIM() dan menyimpan hasilnya

System.out.println("\nHASIL PENCARIAN:"); = menampilkan teks "HASIL PENCARIAN:" ke layar
if (hasilPencarian != null) { = mengecek apakah objek hasilPencarian tidak bernilai null,
System.out.println("Mahasiswa ditemukan!"); = jika ditemukan, tampilkan pesan bahwa mahasiswa ditemukan.
System.out.println(hasilPencarian); = mencetak isi objek Mahasiswa yang ditemukan.
} else { = masuk ke blok else (data tidak ditemukan).
System.out.println("Mahasiswa dengan NIM " + nimCari + " tidak ditemukan."); = menampilkan pesan bahwa mahasiswa dengan NIM yang dicari tidak ada dalam data.
}

scanner.close(); = menutup objek Scanner
}

public static Mahasiswa cariMahasiswaByNIM(Mahasiswa[] daftarMahasiswa, String nim) { = metode static yang menerima array mahasiswa dan NIM yang dicari.
for (int i = 0; i < daftarMahasiswa.length; i++) { = melakukan pencarian linear (satu per satu) pada array mahasiswa
// Bandingkan NIM mahasiswa saat ini dengan NIM yang dicari
if (daftarMahasiswa[i].nim.equals(nim)) { = Jika ditemukan mahasiswa dengan nim yang sama
return daftarMahasiswa[i]; = maka dikembalikan objek mahasiswa tersebut
}
}
// Jika tidak ditemukan
return null; = jika seluruh array sudah dicek dan tidak ditemukan, kembalikan null
}
}


STUDI KASUS 2

import java.util.ArrayList; = mengimpor kelas ArrayList
import java.util.Scanner; = mengimpor kelas Scanner untuk membaca input dari pengguna

class Produk { = mendefinisikan sebuah kelas bernama Mahasiswa
String id; = deklarasi atribut dari kelas nim bertipe String
String nama; = deklarasi atribut nama bertipe String
String kategori; = deklarasi atribut kategori bertipe String
double harga; = deklarasi atribut harga bertipe double
int stok; = deklarasi atribut stok bertipe int

public Produk(String id, String nama, String kategori, double harga, int stok) { = konstruktor dari kelas Produk digunakan untuk mengisi nilai atribut
this.id = id; = mengisi nilai atribut id dengan nilai yang diberikan
this.nama = nama; = mengisi nilai atribut nama dengan nilai yang diberikan
this.kategori = kategori; = mengisi nilai atribut kategori dengan nilai yang diberikan
this.harga = harga; = mengisi nilai atribut harga dengan nilai yang diberikan
this.stok = stok; = mengisi nilai atribut stok dengan nilai yang diberikan
}

@Override = anotasi yang memberi tahu compiler bahwa metode di bawahnya akan meng-override metode yang ada di superclass-nya
public String toString() { = deklarasi metode toString(), yang bertipe String dan bersifat public
return String.format("%-5s | %-25s | %-15s | Rp %.2f | Stok: %d",
                    id, nama, kategori, harga, stok); = mengembalikan sebuah String hasil dari String.format(), yang membuat teks terformat rapi dengan menyisipkan nilai-nilai atribut
}
}

public class PencarianProduk { =  mendeklarasikan kelas publik bernama PencarianProduk
public static void main(String[] args) { = main method
        // Data produk
Produk[] daftarProduk = { = membuat array berisi objek-objek produk. Nama variabelnya adalah daftarProduk
new Produk("P001", "Laptop Asus VivoBook", "Elektronik", 8500000, 10), = membuat objek produk pertama dengan atribut id = P001, nama = Laptop Asus VivoBook, kategori
new Produk("P002", "Smartphone Samsung Galaxy", "Elektronik", 5000000, 15), = membuat objek produk kedua dengan atribut id = P002, nama = Smartphone Samsung Galaxy, kategori
new Produk("P003", "Kemeja Formal Pria", "Fashion", 250000, 50), = membuat objek produk ketiga dengan atribut id = P003, nama = Kemeja Formal P
new Produk("P004", "Sepatu Lari Nike", "Fashion", 1200000, 25), = membuat objek produk keempat dengan atribut id = P004, nama = Sepatu Lari
new Produk("P005", "Buku Pemrograman Java", "Buku", 150000, 30), = membuat objek produk kelima dengan atribut id = P005, nama = Buku Pemrogram
new Produk("P006", "Mouse Gaming Logitech", "Elektronik", 350000, 20), = membuat objek produk keenam dengan atribut id = P006, nama = Mouse Gaming Logitech,
new Produk("P007", "Novel Bumi Manusia", "Buku", 95000, 40), = membuat objek produk ketujuh dengan atribut id = P007, nama = Novel Bumi
new Produk("P008", "Tas Ransel", "Fashion", 300000, 35) = membuat objek produk kedelapan dengan atribut id = P008, nama = Tas R
}; 

Scanner scanner = new Scanner(System.in); = membuat objek Scanner untuk membaca input dari pengguna

System.out.println("=== SISTEM PENCARIAN PRODUK ==="); = menampilkan teks "=== SISTEM PENCARIAN PRODUK ===" k
System.out.println("Kategori tersedia: Elektronik, Fashion, Buku"); = menampilkan teks "Kategori tersedia: Elektronik, Fashion, Buku"
System.out.print("Masukkan kategori produk: "); = menampilkan prompt kepada pengguna untuk memasukkan kategori produk
String kategoriCari = scanner.nextLine(); = membaca input dari pengguna dan menyimpannya ke dalam variabel kategoriCari

System.out.print("Masukkan harga minimum: Rp "); = menampilkan prompt kepada pengguna untuk memasukkan harga minimum
double hargaMin = scanner.nextDouble(); = membaca input dari pengguna dan menyimpannya ke dalam variabel hargaMin

System.out.print("Masukkan harga maksimum: Rp "); = menampilkan prompt kepada pengguna untuk memasukkan harga maksimum
double hargaMax = scanner.nextDouble(); = membaca input dari pengguna dan menyimpannya ke dalam variabel hargaMax

// Lakukan pencarian linear multi-kriteria
ArrayList<Produk> hasilPencarian = cariProdukByKriteria(daftarProduk, kategoriCari, hargaMin, hargaMax); = memanggil metode cariProdukByKriteria() dengan parameter daftarProduk

System.out.println("\nHASIL PENCARIAN:"); = menampilkan teks "HASIL PENCARIAN:"
System.out.println("==============================================================="); = menampilkan garis horizontal
System.out.printf("%-5s | %-25s | %-15s | %-10s | %-10s\n", 
                    "ID", "Nama Produk", "Kategori", "Harga", "Stok"); = menampilkan header tabel dengan format yang rapi
System.out.println("---------------------------------------------------------------"); = menampilkan garis horizontal

if (hasilPencarian.size() > 0) { = jika hasilPencarian tidak kosong
for (Produk p : hasilPencarian) { = melakukan perulangan untuk setiap objek produk di hasilPencarian
    System.out.println(p); = menampilkan informasi produk dengan format yang rapi
}
} else { = jika hasilPencarian kosong
System.out.println("Tidak ada produk yang sesuai dengan kriteria pencarian."); = menampilkan pesan bahwa tidak ada produk yang sesuai dengan kriteria pencarian
}
System.out.println("==============================================================="); = menampilkan garis horizontal

scanner.close(); = menutup objek Scanner untuk menghindari sumber daya yang tidak digunakan
}

public static ArrayList<Produk> cariProdukByKriteria(Produk[] daftarProduk, String kategori, double hargaMin, double hargaMax) { = mendeklarasikan metode cariProdukByKriteria
ArrayList<Produk> hasilPencarian = new ArrayList<>(); = membuat array list kosong untuk menyimpan hasil pencarian

for (int i = 0; i < daftarProduk.length; i++) { = melakukan perulangan untuk setiap objek produk di daftarProduk
    Produk produk = daftarProduk[i]; = membuat variabel produk untuk menyimpan objek produk saat ini

    // Periksa apakah produk memenuhi semua kriteria
if (produk.kategori.equalsIgnoreCase(kategori) && 
                produk.harga >= hargaMin &&
                produk.harga <= hargaMax) {
                hasilPencarian.add(produk); = jika produk memenuhi semua kriteria, maka tambahkan produk tersebut ke dalam hasilPenc
            }
        }

return hasilPencarian; = mengembalikan array list hasilPencarian
    }
}


STUDI KASUS 3

import java.util.ArrayList; = mendeklarasikan import untuk kelas ArrayList
import java.util.Scanner; = mendeklarasikan import untuk kelas Scanner

public class Studi_kasus_3 { = mendeklarasikan kelas Studi_kasus_3
    public static void main(String[] args) { = mendeklarasikan metode main
        Scanner scanner = new Scanner(System.in); = membuat objek Scanner untuk membaca input dari pengguna

        System.out.println("=== SISTEM PENCARIAN KATA ==="); = menampilkan teks "=== SISTEM PENCARIAN KATA ==="
        System.out.print("Masukkan teks: "); = menampilkan prompt kepada pengguna untuk memasukkan teks
        String teks = scanner.nextLine(); = membaca input dari pengguna dan menyimpannya ke dalam variabel teks

        System.out.print("Masukkan kata yang dicari: "); = menampilkan prompt kepada pengguna untuk memasukkan kata yang dicari
        String kataCari = scanner.nextLine(); = membaca input dari pengguna dan menyimpannya ke dalam variabel kataCari

        // Lakukan pencarian kata
        ArrayList<Integer> posisiDitemukan = cariKata(teks, kataCari); = membuat array list kosong untuk menyimpan posisi kata yang ditemukan

        System.out.println("\nHASIL PENCARIAN:"); = menampilkan teks "HASIL PENCARIAN:"
        if (posisiDitemukan.size() > 0) { = jika hasilPencarian tidak kosong
            System.out.println("Kata '" + kataCari + "' ditemukan sebanyak " +posisiDitemukan.size() + " kali pada posisi:"); = menampilkan informasi tentang jumlah dan posisi kata yang ditemukan

            for (int i = 0; i < posisiDitemukan.size(); i++) {
                System.out.println("- Indeks ke-" + posisiDitemukan.get(i) + " (karakter ke-" + (posisiDitemukan.get(i) + 1) + ")"); = menampilkan informasi tentang posisi kata yang ditemukan
            }

            // Tampilkan teks dengan highlight kata yang ditemukan
            System.out.println("\nTeks dengan highlight:"); = menampilkan teks "TEKS DENGAN HIGHLIGHT:"
            tampilkanTeksHighlight(teks, kataCari, posisiDitemukan); = menampilkan teks dengan highlight kata yang ditemukan
        } else { = jika hasilPencarian kosong
            System.out.println("Kata '" + kataCari + "' tidak ditemukan dalam teks."); = menampilkan informasi bahwa kata tidak ditemukan
        }

        scanner.close(); = menutup objek Scanner
    }

    public static ArrayList<Integer> cariKata(String teks, String kata) { = mendeklarasikan metode cariKata
        ArrayList<Integer> posisi = new ArrayList<>(); = membuat array list kosong untuk menyimpan posisi kata yang ditemukan

        // Konversi ke lowercase untuk pencarian case-insensitive
        String teksLower = teks.toLowerCase(); = mengubah teks menjadi lowercase
        String kataLower = kata.toLowerCase(); = mengubah kata menjadi lowercase

        int panjangKata = kataLower.length(); = mendapatkan panjang kata
        int panjangTeks = teksLower.length(); = mendapatkan panjang teks

        // Lakukan linear search
        for (int i = 0; i <= panjangTeks - panjangKata; i++) { = melakukan pencarian linear
            // Periksa apakah substring dari posisi i sampai i+panjangKata sama dengan kata
            String potongan = teksLower.substring(i, i + panjangKata); = mengambil substring dari posisi i sampai i+panjangKata

            if (potongan.equals(kataLower)) { = jika substring sama dengan kata
                posisi.add(i); = menambahkan posisi ke dalam array list posisi

                // Optional: Skip ke akhir kata yang ditemukan untuk menghindari overlap
                // i += panjangKata - 1;
            }
        }

        return posisi; = mengembalikan array list posisi
    }

    public static void tampilkanTeksHighlight(String teks, String kata, ArrayList<Integer> posisi) { = mendeklarasikan metode tampilkanTeksHighlight
        StringBuilder hasil = new StringBuilder(teks); = membuat StringBuilder untuk menyimpan hasil teks dengan highlight

        // Tambahkan marker untuk highlight (dari posisi terjauh dulu untuk menghindari pergeseran indeks)
        for (int i = posisi.size() - 1; i >= 0; i--) { = melakukan perulangan dari belakang
            int pos = posisi.get(i); = mendapatkan posisi
            hasil.insert(pos + kata.length(), "]"); = menambahkan marker ] di sebelah kanan kata
            hasil.insert(pos, "["); = menambahkan marker [ di sebelah kiri kata
        }

        System.out.println(hasil.toString()); = menampilkan hasil teks dengan highlight
    }
}
