
# simple PPh Pasal 21
Aplikasi Simpel menghitung PPH dengan Pasal 21 Menggunakan EcmaScript 6 (JS)

## How's Work?
1. Clone/Download zip Github Repository
2. Open Index.html
3. Done XD

## Explain About PPh Pasal 21
Rumus Dasar dari PPh Pasal 21

    `PPh Pasal 21 = Penghasilan Bruto x Tarif PPh Pasal 17`

Tarif Pajak yang ditetapkan atas penghasilan diatur dalam Undang Undang PPh Paal 17 ayat (1) bagi wajib pajak dalam negeri adalah sebagai berikut :

| Lapisan Penghasilan Kena Pajak | Tarif Pajak |
|--|--|
| Sampai Dengan 50jt | 5% |
| Diatas 50jt dan dibawah sama dengan 250jt | 15% |
| Diatas 250jt dan dibawah sama dengan 500jt | 25% |
| Diatas 500jt | 30% |

## Base Algorithm
1. Input Penghasilan bruto
2. Jika bruto lebih kecil samadengan 50 jt, maka :
   
   `pajakLimaPersen = 50jt x 5%
   pajak =  pajakLimaPersen`

3. Tapi jika bruto diatas 50jt dan dibawah sama dengan 250jt, maka :

   `pajakLimaPersen = 50jt x 5%
   pajakLimaBelasPersen = (bruto - 50jt) x 15%
   pajak = pajakLimaPersen + pajakLimaBelasPersen`

4. Tapi jika bruto diatas 250jt dan dibawah sama dengan 500jt, maka :

   `pajakLimaPersen = 50jt x 5%
   pajakLimaBelasPersen = (bruto - 250jt) x 15%
   pajakDuaLimaPersen = (bruto - ( bruto -250jt - 50jt)) x 0.25
   pajak = pajakLimaPersen + pajakLimaBelasPersen + pajakDuaLimaPersen`

5. Terakhir, jika bruto diatas 500jt, maka :

   `pajakLimaPersen = 50jt x 5%
   pajakLimaBelasPersen = (bruto - 250jt) x 15%
   pajakDuaLimaPersen = (bruto - ( bruto - 500jt)) x 0.25
   pajakTigaPuluh = (bruto - (bruto - ( bruto - 500jt))) x 0.3
   pajak = pajakLimaPersen + pajakLimaBelasPersen + pajakDuaLimaPersen + pajakTigaPuluh`

6. Hasil Pendapatan menjadi,

   `Penghasilan akhir = bruto - pajak`

## Conclusion
Nampaknya memang sedikit rumit, karena jika bruto di atas 500jt misalnya, kita harus menghitung setiap pajak dibawahnya (sesuai batasannya juga) dan pada akhirnya kita mengkalkulasikan keseluruhan tingkat pajak. 
