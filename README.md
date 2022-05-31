# Habit Tracker

> ⏰ Time limit: **150 min**

## Summary

Pada tugas kali ini kalian akan membuat sebuah aplikasi bernama `Habit Tracker`. Dalam aplikasi ini kalian akan menampilkan berbagai macam `Habit` yang kalian tulis. Kalian juga dapat menambahkan `Habit` baru ke dalam list kalian. Silahkan menggunakan `json-server` sebagai database pada aplikasi ini.

Skema dari aplikasi ini adalah sebagai berikut:

```JSON
{
  "habits": [
    {
      "id": 1,
      "name": "Learning Javascript",
      "description": "Learning Javascript is always fun",
      "reward": 100,
      "interval": "daily",
      "startDate": "04/11/2020"
    },
  ]
}
```

> Kalian dibebaskan untuk membuat design dari aplikasi ini selama fitur yang kita minta terpenuhi. Perhatikan juga penempatan element pada aplikasi kalian sehingga nyaman untuk dilihat oleh user 😉

## Competencies

- React
- React Router
- Redux
- Reusable Component

## Release 0

Buatlah sebuah halaman pada path `/` yang akan menampilkan kumpulan `Habit` yang tersedia. Pada setiap item nya akan terdapat data:

- Nama dari `Habit` tersebut.
- Deskripsi dari `Habit` tersebut.
- Interval dari `Habit` tersebut.
- Reward dari `Habit` tersebut.

Di dalam setiap item `Habit` kalian akan terdapat satu button untuk menghapus `Habit` tersebut dari database.

![release-0](./list.png)

### Rules-R0

- Data dari `Habit` wajib didapatkan dari `redux`.
- Fetch data `Habit` dari database harus melalui `action` di redux.

## Release 1

Buatlah sebuah form yang akan menambahkan `Habit` baru kedalam database kita. Kalian dapat membuat halaman baru / membuat modal untuk form ini.

Data yang dapat di input untuk `Habit` baru kita adalah `nama habit`, `deskripsi habit`, `start date habit`, `point reward habit` dan `interval habit` yang merupakan select box dengan pilihan input `Daily`, `Weekly` dan `Monthly`. Gunakanlah textarea untuk menyimpan deskripsi dari `Habit` yang akan kalian buat.

Jika kalian menggunakan halaman baru pastikan user kembali ke halaman `/` ketika berhasil menyimpan data `Habit`.

Pastikan `Habit` yang baru kalian buat sudah terlihat pada list di halaman `/`

![release-1](./add.png)

### Rules-R1

- Menyimpan data `Habit` ke database harus melalui `action` di redux.

## Release 2

Lakukanlah sebuah action ketika user menekan sebuah item yang berada di halaman utama. Action yang akan dilakukan adalah mengarahkan user ke halaman `/habit/:id` yang menampilkan detail dari `Habit` yang dipilih oleh user.

### Notes

Kalian diperbolehkan membuat sebuah button untuk melakukan action ini. Data yang ditampilkan pada halaman `/habit/:id` adalah:

- Nama dari `Habit` tersebut.
- Deskripsi dari `Habit` tersebut.
- Interval dari `Habit` tersebut.
- Reward dari `Habit` tersebut.
- Waktu mulai dari `Habit` tersebut.

![release-2](./detail.png)

### Rules-R2

- Data dari detail `Habit` wajib didapatkan dari `redux`.
- Fetch detail `Habit` dari database harus melalui `action` di redux.

## Release 3

Implementasikan button `delete` pada setiap item di halaman `/` yang akan menghapus data `Habit` tersebut pada database,

### Rules-R3

- Aksi `Delete` harus melalui `action` di redux.
- Data yang berhasil dihapus tidak ditampilkan lagi pada kumpulan `Habit` di halaman `/`

## Release 4

Buatlah halaman dengan path `/daily`, `/weekly`. `/monthly` untuk menampilkan `Habit` yang memiliki inteval sesuai dengan path yang diminta. Pada setiap halaman ini juga terdapat sebuah widget yang akan menampilkan akumulasi `point` untuk setiap habit dengan interval yang dipilih.

![release-4](./daily.png)

> Menurut kalian berapa route yang kalian butuhkan untuk menyelesaikan release ini?

### Rules-R4

- Data dari `Habit` per type wajib didapatkan dari `redux`

## Release 5

Tambahkan validasi sebelum menyimpan habit dengan aturan sebagai berikut:

- `startDate` memiliki format `dd/mm/yyy`.
- `reward` hanya boleh diisi oleh angka.
- Semua input harus terisi sebelum menyimpan data ke database.
- Tampilkan sebuah feedback ketika ada data yang belum terisi pada form,
  feedback ini dapat berbentuk modal/alert tetapi tidak diperbolehkan
  menggunakan fungsi `alert()` javascript.

![release-4](./addError.png)
