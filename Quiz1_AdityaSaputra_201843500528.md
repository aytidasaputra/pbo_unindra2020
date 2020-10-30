## ADITYA SAPUTRA 201843500528
>QUIZ 1 Pemprograman Berbasis Objek

**1.** Void, Return, Konstruktor, This

* **Void** adalah method yang tidak memiliki nilai kembali/return, bisanya digunakan tidak untuk mencari nilai dalam suatu operasi, untuk mendeklarasikannya kita harus menembahkan kata kunci void.

>> Contohnya: 

``` java
    public class App {
    String nama, npm;
    public static void main(String[] args){
        App mhs = new App();
        System.out.println("====== MAHASISWA =======");
        mhs.Mahasiswa();
    }
    
    void Mahasiswa(){
        nama = "Aditya Saputra";
        npm = "201843500528";
        System.out.println("Nama saya :  "+nama);
        System.out.println("Npm saya : "+npm);
    }
}
 ```

* **Return** adalah method yang mengembalikan nilai secara langsung atau sebuah nilai dari variable, cara penulisan method return seperti berikut ini:

>> Contohnya: 

``` java
//TipeData //NamaMethod(){
  return //Nilai yang ingin dikembalikan;
}
```

* **Konstruktor** adalah method khusus yang akan dieksekusi pada saat pembuatan objek (instance).

>> Contohnya:

``` java
public class App {
    public String nama;
    public String npm;

    public User(String nama, String npm){
        this.nama = nama;
        this.npm = npm;
    }
}
```

* **This** Kata kunci this dipergunakan pada pembuatan kelas dan digunakan untuk menyatakan objek sekarang. Untuk menghindari variabel yang sama antara variabel class dengan variabel parameter.

>> Contohnya:

``` java
public String nama;
    public String npm;
    
    public App(String nama, String npm){
        this.nama = nama;
        this.npm = npm;
    }
```

**2.** Syarat - syarat membuat class pada java

Class sebenarnya bertugas untuk mengumpulkan prosedur/fungsi dan variabel dalam satu tempat.

* Memiliki nama kelas
* Membungkus Fungsi dan variabel
* Membuat objek dimain method untuk memanggil class terus tsb

**3.** Buatlah program bebas (tidak boleh sama) dengan menggunakan semua materi yang telah dibahas : (method void, return, konstruktor , keyword "this“) 
**dengan inputan menggunakan scanner !!!**

``` java
import java.util.Scanner;

public class App {
    public String nama, npm, kelas, alamat;

    public App(String nama, String npm) {
        this.nama = nama;
        this.npm = npm;
    }

    public void Mahasiswa(String kelas) {
        this.kelas = kelas;
        System.out.println("NPM MAHASISWA: " + kelas);
    }

    String alamaString(String alamat) {
        return this.alamat = alamat;
    }

}

class pboUnindra {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.println("=== DATA MAHASISWA ===");
        System.out.print("NAMA : ");
        String nama = input.nextLine();
        System.out.print("NPM : ");
        String npm = input.nextLine();

        System.out.print("KELAS : ");
        String kelas = input.nextLine();

        System.out.print("ALAMAT : ");
        String alamat = input.nextLine();

        App mhs = new App(nama, npm);
        mhs.Mahasiswa(kelas);
        

        System.out.println();
        System.out.println("______________________");
        System.out.println("NAMA : " + mhs.nama);
        System.out.println("NPM : " + mhs.npm);
        System.out.println("KELAS : " + kelas);
        System.out.println("ALAMAT : " + mhs.alamaString(alamat));

    }
}
```

**4.** Buat class yang berisi nip nama , golongan, gaji pokok dan tunjuangan seperti gambar disamping (di gambar belum ada nip dan nama)
Buatlah method constructor untuk membuat nama dan nip karyawan
Butlah method dengan outputnya nama , gaji pokok, tunjangan dan total gaji berdasarkan table di samping ( golongan dan sebagai parameter)

``` java
import java.util.Scanner;

public class NomerEmpat {
    String nip;
    String nama;
    String Golongan;
    String gpok;
    String tunjangan;

    public String getNip() {
        return this.nip;
    }

    public void setNip(String nip) {
        this.nip = nip;
    }

    public String getNama() {
        return this.nama;
    }

    public void setNama(String nama) {
        this.nama = nama;
    }

    public String getGolongan() {
        return this.Golongan;
    }

    public void setGolongan(String Golongan) {
        this.Golongan = Golongan;
    }

    public String getGpok() {
        return this.gpok;
    }

    public void setGpok(String gpok) {
        this.gpok = gpok;
    }

    public String getTunjangan() {
        return this.tunjangan;
    }

    public void setTunjangan(String tunjangan) {
        this.tunjangan = tunjangan;
    }

    public static void main(String[] aditya) {
        Scanner input = new Scanner(System.in);
        NomerEmpat data = new NomerEmpat();

        System.out.print("Masukan NIP : ");
        data.setNip(input.nextLine());
        System.out.print("Masukan NAMA : ");
        data.setNama(input.nextLine());
        System.out.print("Masukan Golongan : ");
        data.setGolongan(input.nextLine());
        System.out.print("Masukan Gaji Pokok : ");
        data.setGpok(input.nextLine());
        System.out.print("Masukan Tunjangan: ");
        data.setTunjangan(input.nextLine());

        System.out.println();
        System.out.println("========|DATA KARYAWAN|========");
        System.out.println("NIP :  " + data.getNip());
        System.out.println("NAMA : " + data.getNama());
        System.out.println("GOLONGAN : " + data.getGolongan());
        System.out.println("GAJI POKOK : " + data.getGpok());
        System.out.println("TUNJANGAN : " + data.getTunjangan());
        System.out.println("_______________________________");
    }
}
```

**5.** Buat program utama dalam bentuk pengulangan yang akan berhenti jika jawaban dari anda akan menghitung ulang adalah T.
Buat method static dengan ketentuan nilai akhir adalah uts 30%, uas 50%, tugas+Quiz =20% yang hasilnya seperti gambar disamping

``` java
import java.util.Scanner;

class Mahasiswa {
    private double tugas, quiz, uts, uas, nAkhir;
    private String nama, nim;

    public double getTugas() {
        return tugas;
    }

    public void setTugas(double tugas) {
        this.tugas = tugas;
    }

    public double getQuiz() {
        return quiz;
    }

    public void setQuiz(double quiz) {
        this.quiz = quiz;
    }

    public double getUts() {
        return uts;
    }

    public void setUts(double uts) {
        this.uts = uts;
    }

    public double getUas() {
        return uas;
    }

    public void setUas(double uas) {
        this.uas = uas;
    }

    public String getNama() {
        return nama;
    }

    public void setNama(String nama) {
        this.nama = nama;
    }

    public String getNim() {
        return nim;
    }

    public void setNim(String nim) {
        this.nim = nim;
    }

    double getNilaiAkhir(double tugas,double quiz, double uts, double uas) {
        nAkhir =(0.10 * tugas) + (0.1 * quiz) + (0.3 * uts) + (0.5 * uas);
        return nAkhir;
    }
}

public class NomerLima {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        Mahasiswa oMhs = new Mahasiswa();

        System.out.print("Masukan NAMA: ");
        oMhs.setNama(input.nextLine());
        System.out.print("Masukan NIM: ");
        oMhs.setNim(input.nextLine());
        System.out.print("Masukan Nilai Tugas: ");
        oMhs.setTugas(input.nextDouble());
        System.out.print("Masukan Nilai Quiz: ");
        oMhs.setQuiz(input.nextDouble());
        System.out.print("Masukan Nilai uts: ");
        oMhs.setUts(input.nextDouble());
        System.out.print("Masukan Nilai uas: ");
        oMhs.setUas(input.nextDouble());

        System.out.println("Nama ke " + oMhs.getNama());
        System.out.println("Nim ke " + oMhs.getNim());
        System.out.println("\n");

        double nAkhir = oMhs.getNilaiAkhir(oMhs.getTugas(),oMhs.getQuiz(), oMhs.getUts(), oMhs.getUas());

        System.out.println("Nilai tugas : " + oMhs.getTugas());
        System.out.println("Nilai quiz : " + oMhs.getQuiz());
        System.out.println("Nilai uts : " + oMhs.getUts());
        System.out.println("Nilai uas : " + oMhs.getUas());
        System.out.println("\n");
        System.out.println(oMhs.getNama() + " dengan NIM " + oMhs.getNim() + " memiliki Nilai Akhir " + nAkhir);
        System.out.println("\n");
    }
}
```

**6.**

``` java
public class NomerEnam {
    public static void main(String[] args) {
        for (int i = 0; i < 5; i++) {
            System.out.print(i);
        }
    }
}
```

>>> output

* 1 2 3 4 5
