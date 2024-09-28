# tugas3praktikum2024

A new Flutter project.

Penjelasan Code

AboutPage.dart
File ini menjelaskan AboutPage, yang memberikan informasi mengenai aplikasi.
Komponen Utama:
Imports:

package
/material.dart: Mengimpor pustaka desain material dari Flutter.
package
/homepage.dart: Mengimpor widget HomePage untuk navigasi.
Kelas AboutPage:

StatelessWidget: Menunjukkan bahwa halaman ini tidak memiliki status yang dapat diubah.
Scaffold: Menyediakan struktur dengan AppBar dan body.
AppBar: Menampilkan judul "About Page" dengan latar belakang berwarna biru.
Container: Menampung konten utama dengan latar belakang gradien linier.
Widget Text:
Menampilkan berbagai bagian seperti "Tentang Aplikasi", "Fitur Utama", dan "Versi". Menggunakan TextStyle untuk menyesuaikan font, warna, dan ukuran.

Kelas Sidemenu:
Drawer yang dapat disesuaikan yang mencakup opsi navigasi (Home dan About) menggunakan ListTile. Metode onTap menggunakan Navigator.push untuk berpindah antar layar.

2). Homepage.dart
File ini menjelaskan HomePage, yang berfungsi sebagai halaman utama setelah pengguna login.

Komponen Utama:
Imports:

Mengimpor paket yang diperlukan, termasuk shared preferences untuk menyimpan data serta halaman lainnya.
Kelas HomePage:

StatefulWidget: Menunjukkan bahwa halaman ini dapat mengalami perubahan state (misalnya, data pengguna).
State:

Memuat nama pengguna dari shared preferences saat inisialisasi.
Terdapat metode untuk melakukan logout dan memuat nama pengguna.
AppBar:

Mirip dengan yang ada di AboutPage, tetapi juga menyertakan tombol logout.
Body:

Container: Memiliki latar belakang gradien.
Column: Mengatur pesan sambutan yang menampilkan detail pengguna atau indikator pemuatan.
ElevatedButton: Sebagai placeholder untuk tombol "Get Started" yang dapat digunakan untuk menavigasi ke halaman lain.
Drawer:

Menggunakan kembali Sidemenu untuk navigasi.

3). loginpage.dart

File ini menjelaskan LoginPage, yang bertugas untuk menangani proses otentikasi pengguna.

Komponen Utama:
Imports:

Mengimpor paket yang diperlukan untuk komponen Flutter serta shared preferences.
Kelas LoginPage:

StatefulWidget: Sama seperti HomePage, halaman ini memiliki state yang dapat berubah.
TextEditingController: Digunakan untuk mengelola input dari kolom username dan password.
FormKey: Digunakan untuk memvalidasi input pada form.
Metode:

\_saveUsername: Menyimpan username ke dalam shared preferences.
\_showSnackbar: Menampilkan pesan kepada pengguna.
\_checkLoginStatus: Memeriksa apakah pengguna sudah login saat inisialisasi.
Form:

Memuat kolom teks untuk username dan password dengan validasi.
Menampilkan tombol login yang memeriksa kredensial dengan nilai yang telah ditentukan (admin/admin).
Menyediakan opsi untuk fitur lupa password dan pengalihan ke halaman pendaftaran.

main.dart
File ini berfungsi sebagai titik masuk utama untuk aplikasi Flutter Anda.
Komponen Utama:
Imports:

package
/material.dart: Mengimpor pustaka desain material dari Flutter.
package
/loginpage.dart: Mengimpor halaman login.
Fungsi main():

runApp(const MyApp()): Memulai aplikasi dengan MyApp.
Kelas MyApp:

StatelessWidget: Menunjukkan bahwa widget ini tidak memiliki state yang dapat diubah.
build():

Mengembalikan widget MaterialApp, yang mengonfigurasi tema dan halaman awal aplikasi.
ThemeData: Mengatur palet warna utama menggunakan Colors.deepPurple.
home: Menetapkan halaman awal ke LoginPage.

settingspage.dart
File ini mendeskripsikan halaman pengaturan dalam aplikasi.
Komponen Utama:
Kelas SettingsPage:

StatelessWidget: Halaman ini tidak memiliki state.
Scaffold: Struktur dasar halaman yang mencakup AppBar dan body.
AppBar:
Menampilkan judul "Settings" dengan latar belakang berwarna biru.

Body:

Container: Memiliki latar belakang gradien yang menarik.
Center: Memusatkan konten yang menampilkan teks "Settings Page" dengan gaya font besar dan berwarna putih.

6). sidemenu.dart
File ini menjelaskan menu samping (drawer) untuk navigasi antar halaman.
Komponen Utama:
Imports: Mengimpor halaman yang diperlukan seperti HomePage, AboutPage, dan SettingsPage.

Kelas Sidemenu:

StatelessWidget: Menu ini tidak memiliki state.

Drawer:
Menggunakan ListView untuk menampilkan daftar item.

DrawerHeader: Menampilkan header dengan ikon dan teks sambutan.

ListTile: Menyediakan opsi navigasi untuk Home, About, Settings, dan Logout.

onTap: Menggunakan Navigator.pushReplacement untuk berpindah antar halaman saat item diklik.

Divider: Menyediakan pemisah visual antara item menu.

7)signup.dart

File ini mendeskripsikan halaman pendaftaran pengguna.
Komponen Utama:
Kelas SignUpPage:

StatelessWidget: Halaman ini tidak memiliki state.

Scaffold:

SingleChildScrollView: Memungkinkan konten untuk menggulir jika melebihi batas panjang.

Container: Memiliki latar belakang gradien.

Column: Menyusun elemen secara vertikal, termasuk form pendaftaran.

Input Field:

Menggunakan TextFormField untuk input nama lengkap, email, dan password.

Checkbox: Menunjukkan persetujuan untuk pemrosesan data pribadi.

ElevatedButton: Tombol pendaftaran dengan fungsi placeholder untuk aksi yang akan dilakukan saat ditekan.

Social Media Sign Up: Menggunakan IconButton untuk tombol pendaftaran dengan media sosial (Facebook, Google, Apple).

Tautan untuk Login: Menyediakan opsi untuk kembali ke halaman login jika pengguna sudah memiliki akun.
