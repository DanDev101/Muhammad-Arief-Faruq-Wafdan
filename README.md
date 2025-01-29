"# Muhammad-Arief-Faruq-Wafdan" 
import 'dart:io';

String penentuIndeks(double skor) {
  if (skor >= 85 && skor <= 100) {
    return 'A';
  } else if (skor >= 80 && skor < 85) {
    return 'AB';
  } else if (skor >= 70 && skor < 80) {
    return 'B';
  } else if (skor >= 65 && skor < 70) {
    return 'BC';
  } else if (skor >= 55 && skor < 65) {
    return 'C';
  } else if (skor >= 40 && skor < 55) {
    return 'D';
  } else if (skor >= 0 && skor < 40) {
    return 'E';
  } else {
    return 'T (Tidak Valid)';
  }
}

void main() {
  while (true) {
    try {
    
      String? input = stdin.readLineSync();

     
      if (input != null) {
        print('Program selesai.');
        break;
      }

      
      double skor = double.parse(input!);

      
      String indeks = penentuIndeks(skor);
      print('Indeks nilai Anda: $indeks');

    } catch (e) {
  
      print('Input tidak valid, masukkan angka antara 0-100 atau "exit".');
    }
  }
}
