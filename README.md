# Project-kalkulator-Noveliza

import 'dart:io';

void main() {
  print("=== Kalkulator Sederhana ===");

  // Input angka pertama
  stdout.write("Masukkan angka pertama: ");
  double? num1 = double.tryParse(stdin.readLineSync()!);

  if (num1 == null) {
    print("Input tidak valid. Silakan masukkan angka.");
    return;
  }

  // Input angka kedua
  stdout.write("Masukkan angka kedua: ");
  double? num2 = double.tryParse(stdin.readLineSync()!);

  if (num2 == null) {
    print("Input tidak valid. Silakan masukkan angka.");
    return;
  }

  // Pilih operasi
  print("Pilih operasi:");
  print("1. Penjumlahan (+)");
  print("2. Pengurangan (-)");
  print("3. Perkalian (*)");
  print("4. Pembagian (/)");
  stdout.write("Masukkan pilihan (1/2/3/4): ");
  String? choice = stdin.readLineSync();

  double result;
  switch (choice) {
    case '1':
      result = num1 + num2;
      print("Hasil: $num1 + $num2 = $result");
      break;
    case '2':
      result = num1 - num2;
      print("Hasil: $num1 - $num2 = $result");
      break;
    case '3':
      result = num1 * num2;
      print("Hasil: $num1 * $num2 = $result");
      break;
    case '4':
      if (num2 == 0) {
        print("Kesalahan: Pembagian dengan nol tidak diperbolehkan.");
      } else {
        result = num1 / num2;
        print("Hasil: $num1 / $num2 = $result");
      }
      break;
    default:
      print("Pilihan tidak valid.");
  }

  print("=== Program selesai ===");
}
