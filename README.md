# flightPrice

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        int mesafe, yas, yolculukTipi;
        double mesafeUcreti = 0.10;


        Scanner input = new Scanner(System.in);

        System.out.println("Pozitif sayi olarak mesafe giriniz : ");
        mesafe = input.nextInt();


        System.out.println("pozitif sayi olarak yasinizi giriniz : ");
        yas = input.nextInt();


        System.out.println("Yolculuk tipi giriniz : 1- Tek yon; 2-Gidis-Donus");
        yolculukTipi = input.nextInt();

        if (mesafe > 0 && yas > 0 && yolculukTipi == 1) {
            double total = mesafe * mesafeUcreti;
            System.out.println("indirimsiz toplam : " + total);

            if (yas < 12) {
                total = total * 50 / 100;
                System.out.println("Total :" + total);

            } else if (yas >= 12 && yas <= 24) {
                total = total * 90 / 100;
                System.out.println("Total :" + total);

            } else if (yas > 65) {
                total = total * 70 / 100;
                System.out.println("Total :" + total);
            }
        } else if (mesafe > 0 && yas > 0 && yolculukTipi == 2) {

             double total = mesafe * mesafeUcreti*80/100;

            if (yas < 12) {
                total = total * 50 / 100;
                System.out.println("Total :" + 2*total);

            } else if (yas >= 12 && yas <= 24) {
                total = total * 90 / 100;
                System.out.println("Total :" + 2*total);

            } else if (yas > 65) {
                total = total * 70 / 100;
                System.out.println("Total :" + 2*total);
            }

        }

     else{
        System.out.println("Hatali veri girdiniz. Tekrar deneyiniz");
    }


}
}
