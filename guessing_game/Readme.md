#Rust Guessing Game

https://doc.rust-lang.org/book/ch02-00-guessing-game-tutorial.html

so dari penjelasan di atas katanya kita bakalan ngebikin game tebak2an angka random atau judi SLOT...!!!(matamu a), di mana nantinya kita akan menebak angka 1 sampai 100,

jika angkanya lebih besar dari secret angka maka harus mengulangnya dan bakal di beri tahu kalo angkanya terlalu besar, jika terlalu kecil sebaliknya, dan jika sama maka bakal menang initinya gitulah.

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
- name : adalah nama dari projeknya
- version: adalah versi dari projeknya
- edition: adalah edisinya

- [depedencies]: Menentukan dependensi dari proyek, seperti library atau paket lain yang digunakan dalam proyek.
- rand : adalah nama paket untuk ngebuat random number

ok setelah itu sekarang kita udah tau tentang detail di project ini yaitu nama, versi dan dependencies apa yang kita gunakan let jump in to src/main.rs

```shell

use rand::Rng;
use std::cmp::Ordering;
use std::io;

fn main() {
    println!("Guess the number!");

    let secret_number = rand::thread_rng().gen_range(1..=100);

    loop {
        println!("Please input your guess.");

        let mut guess = String::new();

        io::stdin()
            .read_line(&mut guess)
            .expect("Failed to read line");

        let guess: u32 = match guess.trim().parse() {
            Ok(num) => num,
            Err(_) => continue,
        };

        println!("You guessed: {guess}");

        match guess.cmp(&secret_number) {
            Ordering::Less => println!("Too small!"),
            Ordering::Greater => println!("Too big!"),
            Ordering::Equal => {
                println!("You win!");
                break;
            }
        }
    }
}
```

dari kode di atas saya akan berusaha menjelaskan apa yg sebenernya kode di atas terjadi

- pertama use rand::Rng; apa ini ??
  - ok ini adalah library yg kita pakai untuk ngebikin random number
- line kedua adalah use std::cmp::Ordering; ini adalah standart library dari rust dimana kita bisa mengcompare user value terhadap secret_number value
- line ketiga adalah standart library juga untuk menginput value

sampai sini kita udah tau ada beberapa library yg kita pakai

anjir gua males bgst..!!! sampai sini dulu ya guys
