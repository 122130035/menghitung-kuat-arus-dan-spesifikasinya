#include <iostream>
using namespace std;

int main() {
    // Membaca jumlah data
    int n;
    cout << "Masukkan jumlah data: ";
    cin >> n;

    // Membaca nilai-nilai arus listrik
    float arus[n];
    for (int i = 0; i < n; i++) {
        cout << "Masukkan nilai arus ke-" << i + 1 << ": ";
        cin >> arus[i];
    }

    // Menghitung kuat arus rata-rata
    float total_arus = 0;
    for (int i = 0; i < n; i++) {
        total_arus += arus[i];
    }
    float rata_rata_arus = total_arus / n;

    // Menentukan status kuat arus
    string status;
    if (rata_rata_arus < 1) {
        status = "lemah";
    } else if (rata_rata_arus >= 1 && rata_rata_arus <= 5) {
        status = "sedang";
    } else {
        status = "kuat";
    }

    // Menampilkan hasil
    cout << "=== Hasil Penghitungan Kuat Arus ===" << endl;
    cout << "Data arus listrik: ";
    for (int i = 0; i < n; i++) {
        cout << arus[i] << " ";
    }
    cout << endl;
    cout << "Total arus: " << total_arus << endl;
    cout << "Rata-rata arus: " << rata_rata_arus << endl;
    cout << "Status kuat arus: " << status << endl;

    return 0;
}
