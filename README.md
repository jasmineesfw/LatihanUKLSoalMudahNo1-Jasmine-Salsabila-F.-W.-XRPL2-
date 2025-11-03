# LatihanUKLSoalMudahNo1-Jasmine-Salsabila-F.-W.-XRPL2-
Fungsi dari program ini adalah untuk menghitung biaya total pengiriman paket berdasarkan berat paket, jarak tempuh, dan volume paket. Lalu cara kerjanya adalah dengan cara menginputkan nilai panjang, lebar, dan tinggi oleh user.

Berikut adalah kode programnya:


    
    import java.util.Scanner;
    public class SoalMudahNo1 {
    static double volumePaket(double p, double l, double t) {
        return p * l * t;
    }

    static double biayaPengiriman(double berat, double jarak, double volume) {
        double biayaPerKG;
        double biayaVolume = 0;
        double totalBiaya;

        if(jarak <= 10){
            biayaPerKG = 4250;
        }
        else {
            biayaPerKG = 6000;
        }

        if(volume > 100) {
            biayaVolume = 50000;
        }

        totalBiaya = (biayaPerKG * berat) + biayaVolume;
        return totalBiaya;
    }
    public static void main(String[] args) {
        Scanner inputan = new Scanner(System.in);

        System.out.println("Masukkan Berat Paket (kg): ");
        double berat = inputan.nextDouble();
        System.out.println("Masukkan Jarak Tempuh (km): ");
        double jarak = inputan.nextDouble();
        System.out.println("Masukkan Panjang Paket (cm): ");
        double p = inputan.nextDouble();
        System.out.println("Masukkan Lebar Paket (cm): ");
        double l = inputan.nextDouble();
        System.out.println("Masukkan Tinggi Paket (cm): ");
        double t = inputan.nextDouble();
        double v = volumePaket(p, l, t);
        double total = biayaPengiriman(berat, jarak, v);

        System.out.println("RINCIAN BIAYA PENGIRIMAN");
        System.out.println("Berat Paket = "+ berat +" kg");
        System.out.println("Jarak Tempuh = "+ jarak +" km");
        System.out.println("Volume Paket = "+ v +" cm³");
        System.out.println("Total Biaya Pengiriman = Rp"+ total);

        inputan.close();    
        }
    }
