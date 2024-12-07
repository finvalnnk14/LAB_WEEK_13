Tips week 13:
1. cara ubah nama package di refactor -> rename
2. kalau R error perlu import R (tinggal tekan alt + enter di R yg error)
3. no 10 di module itu avtivity_main.xml
4. bagian:
   <androidx.constraintlayout.widget.ConstraintLayout>
   ...
   </androidx.constraintlayout.widget.ConstraintLayout>
   itu maksudnya kode dari week 12
5. dibawahnya langsung ke kode
   <data>
   <variable
   name="viewModel"
   type="com.example.lab_week_13.MovieViewModel" />
   </data>
   kode yang ini ga usah ditulia lg:
   <androidx.constraintlayout.widget.ConstraintLayout>
   ...
   </androidx.constraintlayout.widget.ConstraintLayout>
6. kalau ada yang sama dibagian <androidx.constraintlayout.widget.ConstraintLayout> kode nya di hapus, jangan lupa </layout>
7. di file main activity.kt kalian bagian set content vie copas aja kode dibawah ini:
   val binding: ActivityMainBinding = DataBindingUtil
   .setContentView(this, R.layout.activity_main)
8. kode dibawah ini:
   binding.viewModel = movieViewModel
   binding.lifecycleOwner = this
   letakin di bawah kode ini:
   })[MovieViewModel::class.java]
9. kode dibawah ini:
10. @Entity(tableName = "movies", primaryKeys = [("id")])
    letakin disetelah import2
11. kode dibawah ini:
    data class Movie(...)
   artinya dari kode week 12
12. kode dibawah ini:
    private val movieDatabase: MovieDatabase
    letakin disebalah kode private val movieService: MovieService,
    NOTE: JANGAN LUPA KASIH TANDA KOMA (,)
13. kode dibawah ini:
    val constraints = Constraints.Builder()
   dibawah kode:
    // create a MovieDatabase instance
        val movieDatabase =
            MovieDatabase.getInstance(applicationContext)
        // create a MovieRepository instance
        movieRepository =
            MovieRepository(movieService, movieDatabase)

