#Rust Guessing Game

https://doc.rust-lang.org/book/ch02-00-guessing-game-tutorial.html

so dari penjelasan di atas katanya kita bakalan ngebikin game tebak2an angka random atau judi SLOT...!!!(matamu a), di mana nantinya kita akan menebak angka 1 sampai 100,

jika angkanya lebih besar dari angka maka harus mengulangnya dan bakal di beri tahu kalo angkanya terlalu besar, jika terlalu kecil sebaliknya, dan jika sama bakal menang initinya gitulah.

lanjut ke pembahasan kodenya line by line kita mulai dari Cargo.toml

```shell
[package]
name = "guessing_game"
version = "0.1.0"
edition = "2021"

# See more keys and their definitions at https://doc.rust-lang.org/cargo/reference/manifest.html

[dependencies]
rand = "0.8.5"
```

- [package]:menentukan informasi dasar serperti nama, versi, dan deskripsi dari proyek, ini kek package.json itu lho cuy.
- name : adalah nama dari projeknya version: adalah versi dari projeknya
- edition: adalah edisinya

- [depedencies]: Menentukan dependensi dari proyek, seperti library atau paket lain yang digunakan dalam proyek.
- rand : adalan paket untuk ngebuat random number

// bantu nulis lah bangsat...! males
