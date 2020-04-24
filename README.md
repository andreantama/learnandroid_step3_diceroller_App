# LEARNANDROID STEP3 DICE ROLLER APP
1. Belajar membuat layout di activity_main.xml dengan belajar hal baru : 
   - android:layout_gravity : 
      - center_verticaly
      - center_horizontaly
2. Pada view ImageView ada attribute tools:src="@drawable/dice_1" yang digunakan untuk menampilkan gambar hanya pada saat develop / preview di android studio.
3. Menampilkan gambar dengan exstension .XML, yang memiliki keuntungan apabila scale gambar ditinggikan, kualitas gambar akan tetap bagus
   TETAPI exstension ini hanya dapat digunakan untuk android versi 21(lolipop) minimal. Apabila android versi dibawah 21 dapat menggunakan
   .XML extension ini dengan menggunakan cara :
   - di bulid.gradle (app) menambahkan vectorDrawables.useSupportLibrary = true di dalam defaultConfig
   - Di ViewGroup ditambahkan attribute dan value ini xmlns:app="http://schemas.android.com/apk/res-auto" (Menambhkan Namespace app)
   - di View ImageView merubah attribute android:src menjadi app:srcCompat.
4. Memanggil id di activity_main.xml di MainActivity.kt dengan konsep kerja (ViewObject in memory -> R class -> MainActivity.kt)
5. Mengganti source gambar di MainActiviy.kt dengan cara resultDice.setImageResource(resultImage).
6. Android Compatibility Strategi
   - Setiap versi android memiliki fitur terbaru dan fungsi terbaru.
   - mmengatur minimanVersion adalah perlu diperhitungkan karena ada beberapa fitur di android versi lama tidakada di versibaru atau 
     sebaliknya sehingga dapat menyebabkan crash.
