# Proyek Akhir Pemrograman Berbasis Objek 1

Proyek ini adalah contoh sederhana aplikasi Transaksi Laundry menggunakan Java sebagai tugas akhir dari mata kuliah pemrograman berbasis objek 1.

## Deskripsi

Aplikasi ini menerima input berupa namaPelanggan,beratPakaian,layanan dan memberikan output berupa total harga

Aplikasi ini mengimplementasikan beberapa konsep penting dalam pemrograman berorientasi objek (OOP) seperti Class, Object, Atribut, Method Constructor, Method Mutator, Method Accessor, Encapsulation, Inheritance, Overloading, Overriding, Seleksi, Perulangan, IO Sederhana, Array, dan Error Handling.

## Penjelasan Kode

Berikut adalah bagian kode yang relevan dengan konsep OOP yang dijelaskan:

1. **Class** adalah template atau blueprint dari object. Pada kode ini, `Laundry`, `LaundryDetail`, dan `LaundryBeraksi` adalah contoh dari class.

```bash
public class Laundry {
    ...
}

public class LaundryDetail extends Laundry {
    ...
}

public class LaundryBeraksi {
    ...
}
```

2. **Object** adalah instance dari class. Pada kode ini, `transaksi[0] = new LaundryDetail(namaPelanggan,beratPakaian,Layanan);` adalah contoh pembuatan object.

```bash
transaksi[0] = new LaundryDetail("Novita", 3.5, "cuci kering");
```

3. **Atribut** adalah variabel yang ada dalam class. Pada kode ini, `namaPelanggann` ,`beratPakaian`, `layanan` adalah contoh atribut.

```bash
String namaPelanggan;
double beratPakaian;
String layanan;
double totalHarga;
```

4. **Constructor** adalah method yang pertama kali dijalankan pada saat pembuatan object. Pada kode ini, constructor ada di dalam class `Laundry` dan class 'LaundryDetail' .

```bash
public Laundry(String namaPelanggan, double beratPakaian, String layanan) {
        this.namaPelanggan = namaPelanggan;
        this.beratPakaian = beratPakaian;
        this.layanan = layanan;
        hitungTotalHarga();
}
public LaundryDetail(String namaPelanggan, double beratPakaian, String layanan) {
        super(namaPelanggan, beratPakaian, layanan);
    
}
```

5. **Mutator** atau setter digunakan untuk mengubah nilai dari suatu atribut. Pada kode ini, `setNamaPelanggan` , `setBeratPakaian` ,'setLayanan' ,'hitungTotalHarga adalah contoh method mutator dan perhitungan.

```bash
// Mutator untuk namaPelanggan
    public void setNamaPelanggan(String namaPelanggan) {
        this.namaPelanggan = namaPelanggan;
    }

    // Mutator untuk beratPakaian
    public void setBeratPakaian(double beratPakaian) {
        this.beratPakaian = beratPakaian;
        hitungTotalHarga();
    }
// Mutator untuk layanan
    public void setLayanan(String layanan) {
        this.layanan = layanan;
        hitungTotalHarga();
        
    } 
//perhitungan
    private void hitungTotalHarga() {
        switch (layanan.toLowerCase()) {
            case "cuci kering" -> totalHarga = 5000 * beratPakaian;
            case "cuci setrika" -> totalHarga = 9000 * beratPakaian;
            case "setrika" -> totalHarga = 4000 * beratPakaian;
            default -> {
                System.out.println("Layanan tidak tersedia");
                totalHarga = 0; // Set total harga menjadi 0 jika layanan tidak valid
            }
        }
```

6. **Accessor** atau getter digunakan untuk mengambil nilai dari suatu atribut. Pada kode ini, `getNamaPelanggan`, `getBeratPakaian`, `getLayanan`, dan `getTotalHarga` adalah contoh method accessor.

```bash
// Accessor untuk namaPelanggan
    public String getNamaPelanggan() {
        return namaPelanggan;
    }
    // Accessor untuk beratPakaian
    public double getBeratPakaian() {
        return beratPakaian;
    }
     // Accessor untuk layanan
    public String getLayanan() {
        return layanan;
    }
    // Accessor untuk totalHarga
    public double getTotalHarga() {
        return totalHarga;
    }
```

7. **Encapsulation** adalah konsep menyembunyikan data dengan membuat atribut menjadi private dan hanya bisa diakses melalui method. Pada kode ini, atribut `namaPelanggan` , `beratPakaian`,'layanan'  dan'totalHarga' dienkapsulasi dan hanya bisa diakses melalui method getter dan setter.

```bash
    private String namaPelanggan;
    private double beratPakaian; 
    private String layanan;
    private double totalHarga;
```

8. **Inheritance** adalah konsep di mana sebuah class bisa mewarisi property dan method dari class lain. Pada kode ini, `LaundryDetail` mewarisi `Laundry` dengan sintaks `extends`.

```bash
public class LaundryDetail extends Laundry {
    ...
}
```

9. **Polymorphism** adalah konsep di mana sebuah nama dapat digunakan untuk merujuk ke beberapa tipe atau bentuk objek berbeda. Ini memungkinkan metode-metode dengan nama yang sama untuk berperilaku berbeda tergantung pada tipe objek yang mereka manipulasi, polymorphism bisa berbentuk Overloading ataupun Overriding. Pada kode ini, method `displayInfo(String)` di `Laundry` merupakan overloading method `displayInfo` dan `displayInfo` di `LaundryDetail` merupakan override dari method `displayInfo` di `Laundry`.

```bash
//polymorphinm 
    @Override
    public String toString() {
        return "LaundryDetail{" +
                "namaPelanggan='" + getNamaPelanggan() + '\'' +
                ", beratPakaian=" + getBeratPakaian() +
                ", layanan='" + getLayanan() + '\'' +
                ", totalHarga=" + getTotalHarga() +
                '}';
    }
```

10. **Seleksi** adalah statement kontrol yang digunakan untuk membuat keputusan berdasarkan kondisi. Pada kode ini, digunakan seleksi `if else` dalam method `getBeratPakaian` dan seleksi `switch` dalam method `getLayanan`.

```bash
public String getBeratPakian() {
  if (beratPakaian <= 0) {
                    System.out.println("Berat pakaian harus lebih dari 0 kg");
                    lanjutkan = false;  

    //

String layanan = "";
     switch (kodeLayanan) {
        case 1:
            layanan = "cuci kering";
               break;
        case 2:
            layanan = "cuci setrika";
                break;
        case 3:
            layanan = "setrika";
                 break;
                    default:
     System.out.println("Kode layanan tidak valid");
        lanjutkan = false; 
                  break;
}
```

11. **Perulangan** adalah statement kontrol yang digunakan untuk menjalankan blok kode berulang kali. Pada kode ini, digunakan loop `for` untuk meminta input dan menampilkan data.

```bash
for (int i = 0; i < jumlahTransaksi; i++)  {
    ...
}
```

12. **Input Output Sederhana** digunakan untuk menerima input dari user dan menampilkan output ke user. Pada kode ini, digunakan class `Scanner` untuk menerima input dan method `System.out.println` untuk menampilkan output.

```bash
Scanner scanner = new Scanner(System.in);
        boolean lanjutkan = true;
        int maxTransaksi = 10;

System.out.print("Masukkan nama pelanggan: ");
                String namaPelanggan = scanner.nextLine();

                System.out.print("Masukkan berat pakaian (kg): ");
                double beratPakaian = scanner.nextDouble();
                scanner.nextLine(); 
```

13. **Array** adalah struktur data yang digunakan untuk menyimpan beberapa nilai dalam satu variabel. Pada kode ini, `LaundryDetail[] transaksi = new LaundryDetail[maxTransaksi];` adalah contoh penggunaan array.

```bash
 LaundryDetail[] transaksi = new LaundryDetail[maxTransaksi];
```

14. **Error Handling** digunakan untuk menangani error yang mungkin terjadi saat runtime. Pada kode ini, digunakan `try catch` untuk menangani error.

```bash
//eror handling
        do {
            try {
                System.out.print("Masukkan nama pelanggan: ");
                String namaPelanggan = scanner.nextLine();

                System.out.print("Masukkan berat pakaian (kg): ");
                double beratPakaian = scanner.nextDouble();
                scanner.nextLine(); 
                
                // Validasi input berat pakaian
                if (beratPakaian <= 0) {
                    System.out.println("Berat pakaian harus lebih dari 0 kg");
                    lanjutkan = false; 
                }

                System.out.println("Pilih layanan:");
                System.out.println("1. Cuci Kering (Rp 5000 per kg)");
                System.out.println("2. Cuci Setrika (Rp 9000 per kg)");
                System.out.println("3. Setrika (Rp 4000 per kg)");
                System.out.print("Masukkan kode layanan (1/2/3): ");
                int kodeLayanan = scanner.nextInt();
                scanner.nextLine(); 
//seleksi
     String layanan = "";
     switch (kodeLayanan) {
        case 1:
            layanan = "cuci kering";
               break;
        case 2:
            layanan = "cuci setrika";
                break;
        case 3:
            layanan = "setrika";
                 break;
                    default:
     System.out.println("Kode layanan tidak valid");
        lanjutkan = false; 
                  break;
                }

        if (lanjutkan) {
// Buat objek LaundryDetail
    LaundryDetail laundry = new LaundryDetail(namaPelanggan, beratPakaian, layanan);
                    
// Simpan transaksi ke dalam array
    transaksi[jumlahTransaksi] = laundry;
    jumlahTransaksi++;

// Tampilkan detail laundry dan total harga
    System.out.println("\nDetail Laundry:");
    System.out.println("Nama Pelanggan: " + laundry.getNamaPelanggan());
    System.out.println("Berat Pakaian: " + laundry.getBeratPakaian() + " kg");
    System.out.println("Layanan: " + laundry.getLayanan());
    System.out.println("Total Harga: Rp " + laundry.getTotalHarga());

// Tanya pengguna apakah ingin melanjutkan
    System.out.print("\nApakah Anda ingin melakukan input lagi? (ya/tidak): ");
    String jawaban = scanner.nextLine();
    if (!jawaban.equalsIgnoreCase("ya")) {
       lanjutkan = false;
                    }
                }
    } catch (InputMismatchException e) {
    System.out.println("Input yang dimasukkan tidak valid. Masukkan angka untuk berat pakaian atau kode layanan.");
    scanner.nextLine(); 
          lanjutkan = false; 
         }

## Usulan nilai

| No  | Materi         |  Nilai  |
| :-: | -------------- | :-----: |
|  1  | Class          |    5    |
|  2  | Object         |    5    |

|  3  | Atribut        |    5    |
|  4  | Constructor    |    5    |
|  5  | Mutator        |    5    |
|  6  | Accessor       |    5    |
|  7  | Encapsulation  |    5    |
|  8  | Inheritance    |    5    |
|  9  | Polymorphism   |   10    |
| 10  | Seleksi        |    5    |
| 11  | Perulangan     |    5    |
| 12  | IO Sederhana   |   10    |
| 13  | Array          |   15    |
| 14  | Error Handling |   15    |
|     | **TOTAL**      | **100** |

## Pembuat

Nama: Novita Fitria Ratnaewati
NPM: 2210010228
