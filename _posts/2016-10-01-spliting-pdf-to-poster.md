---
layout: post
title: Membuat PDF jadi Poster
date: 2016-10-01 00:00:00
categories: 'How-To'
---

Aku menemukan satu program yang berguna bernama pdfposter. Program ini menghasilkan poster berukuran besar dengan menggabungkan banyak halaman.
Input yang diterima berupa file format PDF satu halaman dan menghasilkan file PDF multi-halaman.

File gambar bisa dibuat menjadi file PDF satu halaman dengam mudah menggunakan program [Scribus](https://www.scribus.net/).

### Installasi pdfposter

``` terminal
$ sudo [your package manager] install pdfposter
```

Install menggunakan package manager (apt, dnf) pada sistem kamu, dengan nama paket yaitu pdfposter.

### Penggunaan

```terminal
$ pdfposter -p2x2a4 input.pdf poster.pdf
```

Program akan menghasilkan file pdf 2x2 (4) halaman dengan ukuran halaman A4. Input file bernama input.pdf dan output file bernama poster.pdf.
Untuk contoh penggunaan dan informasi perintah lainnya silahkan membaca dokumentasinya.


### Hasil
![Poster hasil](/public/images/2016/10/01/poster.jpg)


### Referensi

[PDF Poster Documentation](https://pythonhosted.org/pdftools.pdfposter/)   
[Git Repo at Gitlab](https://gitlab.com/pdftools/pdfposter)
[AUR](https://aur.archlinux.org/packages/pdfposter-git/)   
