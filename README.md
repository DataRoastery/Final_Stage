![image](https://github.com/DataRoastery/Final_Stage/assets/132192429/8e65b13d-4b84-46b7-ab3e-4e529bf7deb6)# Final_Project Stage 1 Data Roastery

## 1. Descriptive Statistics
Kesimpulan :
- Fitur dengan right skew atau positive skew adalah Age, AnnualIncome, ChronicDiseasses, dan TravelInsurance.
- Fitur dengan left skew atau negative skew adalah FamilyMembers
- Unnamed: 0 tidak disebutkan dalam kedua skew tersebut karena kami menganggap fitur ini sebagai index.
- Fitur EmploymentType memiliki data terbanyak pada Private Sector/ Self Employed dengan jumlah data 1417 .
- Fitur GraduateOrNot memiliki data terbanyak pada kategori Yes dengan jumlah data 1692.
- Fitur FrequentFlyer memiliki data terbanyak pada kategori No dengan jumlah data 1570.
- Fitur EverTravelledAbroad memiliki data terbanyak pada kategori No dengan jumlah data 1607.

## 2. Univariate Analysis
Kesimpulan : 
- Tidak terdapat outlier pada data numerical, sehingga tidak perlu dilakukan handling outliers pada stage data preprocessing
- Age distribusi bimodal perlu dilakukan feature transformation pada stage data preprocessing untuk menjamin kualitas dari algoritma
  annualIncome distribusi mendekati normal
- familyMembers skew kanan perlu dilakukan feature transformation pada stage data preprocessing untuk menjamin kualitas dari algoritma
- ChronicDiseases dan TravelInsurance perlu diubah tipe datanya menjadi categorical, dikarenakan ChronicDiseases dan TravelInsurance hanya berisi 1 dan 0
-Semua fitur kategorik merupakan kategori biner. Untuk sekarang tiidak ada yang tindakan lebih lanjut yang perlu dilakukan 
- Tidak ada class imbalanced

## 3. Univariate Analysis
Kesimpulan : 
- Dari hasil Striplot terlihat cukup konsisten antara feature EverTraveledAbroad,FrequentFlyer, AnnualIncome dengan label (TravelInsurance)
- Terdapat pasang-pasangan feature yang berkorelasi satu sama lain yaitu :
    * FreqentFlyer dan Annual Income (0.35) 
    * EverTravelledAbroad dan Annual Income(0.49)
    * EmploymentType dan Annual Income (-0.35)
      (EmplomentType : Private Sector/Self Employed berkorelasi positif dengan Annual Income, Government Sector berkorelasi negatif dengan Annual Income)
    * EverTravelledAbroad dan FrequentFlyer(0.28)
- Sedangkan feature-feature yang memiliki korelasi tinggi dengan label :
    * TravelInsurance dan Annual Income(0.40)
    * TravelInsurance dan FrequentFlyer(0.23)
    * TravelInsurance dan EverTravelledAbroad(0.43)
Rekomendasi : 
untuk heatmap, tidak ada fitur yang redundant >0.7, jadi tidak perlu ada fitur yang dihilangkan 
untuk antar feature yang memiliki korelasi tinggi, bisa di explore lebih lanjut

## 4. Business Insight
- Menargetkan promo penawaran terhadap target pelanggan dengan kriteria
  * bekerja di private sector/self employment.
  * memiliki annual income diatas 1.3M.
  * merupakan lulusan perguruan tinggi.
  * pernah melakukan perjalanan keluar negeri.
  * Sering melakukan penerbangan.
- Melakukan pembagian umur menjadi 3 kategori dan promo penawaran dengan target pelanggan yang berumur kurang dari 26 tahun dan diatas 33 tahun.
- Membuat prioritas terhadap pelanggan dengan kriteria :
  * Memprioritaskan penawaran kepada pelanggan yang bekerja di private sector, memiliki annual income diatas 1,3M dan berumur diatas 28 tahun.
  * Memiliki annual income lebih dari 1.3M pada semua rentang umur.
  * Punya anggota keluarga sebanyak 4 orang  karena tingkat risiko yang tinggi akibat sait dan tanggungan keluarga.
  * Mempunyai anggota keluarge sebanyak 5 orang di bawah umur 28 tahun dan yang terdiri dari 4 orang pada umur 26-32 tahun.








