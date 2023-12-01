# Tgsmobile10
Nama : Tyanshi Firli Maharani 

NIM : 312210581

Kelas : TI.22.A5

Mata Kuliah : Pemrograman Mobile 1

Dosen Pengampu : Donny Maulana, S.Kom.,M.M.S.I.

Tugas :
Buatlah tampilan menu Versi 02 dari project-project yang sudah dibuat sebelumnya

dengan tambahan memanggil method Maps

dengan tampilan sebagai berikut :

![logo image](https://github.com/firlimaharani/Tgsmobile10/assets/130529482/1f4f09aa-e530-4463-babc-e2f876e65113)
launcherlogo

1. Menu Utama
Pertama yang harus kita lakukan adalah mengganti tampilan menu utamanya dengan code yang baru agar ikon tombol berubah menjadi gambar, caranya adalah : Jika awal pembuatan project kita memilih template Empty Views Activity, maka pada layout otomatis terbuat file activity_main.xml dan pada java akan ada MainActivity.java. Maka langsung saja kita buka activity_main.xml, dan buat code seperti berikut ini:

'''
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="@drawable/gb3"
    tools:context=".home">

    <TextView
        android:id="@+id/imageView"
        android:layout_width="0dp"
        android:layout_height="0dp"
        android:layout_marginTop="30dp"
        android:text="Firly Maharani"
        android:textAlignment="center"
        android:textColor="@color/white"
        android:textSize="50dp"
        android:textStyle="italic"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.476"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.004" />

    <ImageButton
        android:id="@+id/button_move_hallo"
        android:layout_width="48dp"
        android:layout_height="48dp"
        android:background="@drawable/hello"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.112"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.269" />

    <ImageButton
        android:id="@+id/button_move_count"
        android:layout_width="48dp"
        android:layout_height="48dp"
        android:background="@drawable/calculate"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.388"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.269" />

    <ImageButton
        android:id="@+id/button_move_to_other_scroll"
        android:layout_width="48dp"
        android:layout_height="48dp"
        android:background="@drawable/scroll"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.641"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.269" />

    <ImageButton
        android:id="@+id/buttonMoveToOtherActivity"
        android:layout_width="48dp"
        android:layout_height="48dp"
        android:layout_alignParentBottom="true"
        android:layout_centerHorizontal="true"
        android:background="@drawable/two"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.9"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.269" />

    <ImageButton
        android:id="@+id/button_move_to_alarm"
        android:layout_width="48dp"
        android:layout_height="48dp"
        android:background="@drawable/jam"
        android:onClick="moveToAnotherActivity"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.112"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.431"
        tools:ignore="SpeakableTextPresentCheck" />

    <ImageButton
        android:id="@+id/button_map"
        android:layout_width="48dp"
        android:layout_height="48dp"
        android:background="@drawable/map"
        android:onClick="map"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.388"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.43"
        tools:ignore="SpeakableTextPresentCheck" />


</androidx.constraintlayout.widget.ConstraintLayout>

Maka tampilan menu utama akan seperti ini : 
![WhatsApp Image 2023-12-01 at 08 09 37](https://github.com/firlimaharani/Tgsmobile10/assets/130529482/ec011bc3-47df-4d03-97a8-68e093bd7c82)
'''
Setelah itu kita buka MainActivity.java untuk menambahkan code intent untuk masing-masing tombol :
package com.example.mobile_icon;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }
}
Button HelloWorld, Count, Sianida dan TwoActivity menggunakan Explicit Intent, dan untuk project SetAlarm beserta Maps menggunakan Implicit Intent. Menu halaman utama dan tombol-tombol aplikasi sudah berhasil dibuat. Maka selanjutnya yang kita lakukan adalah menambahkan coding pada AndroidManifest.xml agar aplikasi dapat berjalan.

2. AndroidManifest.xml
Didalam AndroidManifest.xml kita tambahkan semua java class dari semua project kita sebelumnya. Berikut nama java class dari berbagai project yang telah saya buat: a. Project Hello World = HelloActivity.java b. Project Count = CountActivity.java c. Project Scroll Movie = SianidaActivity.java d. Project TwoActivity = TwoActivity.java dan Two2Activity.java e. Project Set Alarm = MainActivity.java f. Project Maps = MainActivity.java (karena merupakan Implicit Intent, jadi code untuk SetAlarm dan Maps langsung dibuat disini)

'''
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools">

    <uses-permission android:name="android.permission.POST_NOTIFICATIONS" />
    <uses-permission android:name="android.permission.VIBRATE" />


    <application
        android:allowBackup="true"
        android:dataExtractionRules="@xml/data_extraction_rules"
        android:fullBackupContent="@xml/backup_rules"
        android:icon="@drawable/splash3"
        android:label="@string/app_name"
        android:roundIcon="@drawable/splash1"
        android:supportsRtl="true"
        android:theme="@style/Base.Theme.Mobile_icon"
        tools:targetApi="31">
        <activity
            android:name=".home"
            android:exported="false" />
        <activity
            android:name=".MainActivity"
            android:exported="true" />
        <activity
            android:name=".SetAlarm"
            android:exported="true" />

        <receiver android:name=".AlarmReceiver" />

        <activity
            android:name=".activitySplash"
            android:exported="true">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
        <activity android:name=".FiboActivity" />
        <activity android:name=".scrollActivity" />
        <activity android:name=".pertamaActivity" />
        <activity android:name=".KeduaActivity" />
        <activity
            android:name=".MapActivity"
            android:exported="false"/>
    </application>

</manifest>
3. Code All Projects (XML files / res)
Pada menu values :

'''
Strings.xml
<resources>
    <string name="app_name">ProjectZulaeha</string>
    <string name="Hello_World">Hello World!!</string>
    <string name="button_main">Send</string>
    <string name="editText_main">Enter Your Message Here</string>
    <string name="text_header">Message Received</string>
    <string name="buttton_second">Reply</string>
    <string name="editText_second">Enter Your Reply Here</string>
    <string name="text_header_reply">Reply Received</string>
    <string name="button_label_toast">Toast</string>
    <string name="button_label_count">Count</string>
    <string name="count_initial_value">1</string>
    <string name="toast_massage">Hello Toast!</string>
    <string name="button_label_restart">Restart</string>
    <string name="enter_fibonacci_limit">Masukkan Angka Limit</string>
    <string name="article_title"> Kasus Sianida</string>
    <string name="article_subtitle">ICE COLD!</string>
    <string name="article_text"> Film dokumenter Ice Cold: Murder, Coffee and Jessica Wongso memaparkan pertanyaan tak terjawab tentang persidangan yang dilalui Jessica Wongso. Dengan menyajikan perspektif baru, film ini hadir bertahun-tahun setelah kematian sahabat Jessica, Wayan Mirna Salihin.
Film ini menggambarkan bagaimana Jessica yang mengajak teman-temannya, termasuk Mirna, untuk bertemu setelah sekian lama tak berjumpa. Pertemuan di salah satu kafe di mal ibu kota tersebut pun berlangsung lancar, sebelum akhirnya Mirna pingsan sesaat setelah meminum kopi yang sebelumnya dipesan Jessica.Dokumenter ini turut menyajikan rekaman CCTV pada waktu kejadian, berbagai footage berita saat persidangan berlangsung, hingga wawancara eksklusif dengan beberapa sumber, termasuk Jessica Wongso.
Persidangan atas dugaan pembunuhan Mirna Salihin digelar lima bulan setelah kematiannya. Sidang tersebut melalui 32 kali persidangan dengan menghadirkan puluhan saksi di pengadilan. Hasilnya, Jessica Wongso divonis bersalah atas kematian Mirna dan dijatuhi hukuman 20 tahun penjara.
Kasus yang berjalan cukup lama tersebut menyita banyak perhatian dari masyarakat Indonesia. Musababnya, banyak misteri tak terjawab selama rangkaian persidangan yang panjang tersebut. Salah satunya adalah mengenai akses untuk mendapatkan bubuk sianida yang tidak bisa didapatkan oleh orang sembarangan. Selain itu, motif Jessica di balik pembunuhan tersebut pun belum menemukan jawabannya.
Film dokumenter buatan Netflix ini menyoroti rangkaian persidangan yang saat itu menjadi sidang pertama yang disiarkan secara langsung di berbagai stasiun televisi Indonesia. Selain itu, kasus ini juga diliput secara intens oleh media massa, baik nasional maupun internasional.Tak hanya itu, pihak rumah produksi Beach House Pictures juga berhasil mendapatkan akses untuk mewawancarai Jessica Wongso secara langsung dari balik tahanan. Dalam video trailer yang diluncurkannya, ditampilkan juga sejumlah wawancara eksklusif yang dilakukan dengan beberapa narasumber. Mulai dari ayah dan saudara kembar  Mirna Salihin, pengacara Jessica Wongso, jurnalis yang mendalami kasus tersebut, hingga bagaimana saat itu kasus ini begitu ramai diberitakan oleh media massa Indonesia dan internasional.</string>
</resources>

Colors.xml
'''
<?xml version="1.0" encoding="utf-8"?>
<resources>
    <color name="black">#FF000000</color>
    <color name="white">#FFFFFFFF</color>
    <color name="blue">#3700B3</color>
    <color name="pink">#FFC0CB</color>
    <color name="colorPrimary">#3F5185</color>
    <color name="colorPrimaryDark">#303F9F</color>
    <color name="colorAccent">#FF4081</color>
    <color name="salem">#F8C6E6</color>
    <color name ="purple">#E3A2ED</color>
    <color name="biru">#8FC2EA</color>
    <color name="hijaumuda">#C2E69C</color>
    <color name="cream">#E6C18A</color>
    <color name="coklat">#65362c</color>
    <color name="abu">#B0B0B2</color>
    <color name="tosca">#70AE98</color>
    <color name="soft">#AED9EA</color>
    <color name="pastel">#5E96AE</color>
</resources>
Dimens.xml
'''
<?xml version="1.0" encoding="utf-8"?>
<resources>
    <dimen name="padding_regular">10dp</dimen>
    <dimen name="line_spacing">5sp</dimen>
</resources>
Pada menu themes :

themes.xml
<resources xmlns:tools="http://schemas.android.com/tools">
    <!-- Base application theme. -->
    <style name="SplashScreen" parent="Theme.MaterialComponents.DayNight.NoActionBar">
        <item name="android:windowBackground">@drawable/splashscreen</item>
        <item name="android:statusBarColor">?attr/colorOnPrimary</item>
    </style>
</resources>
Pada menu drawable :

backgroundlauncher.xml
<?xml version="1.0" encoding="utf-8"?>
<layer-list xmlns:android="http://schemas.android.com/apk/res/android">
    <item android:drawable="@color/birumuda"/>
    <item>
        <bitmap
            android:src="@drawable/logo"
            android:gravity="center" />
    </item>
</layer-list>
A. Code Project Hello World
A. Code Project Splash Screen
'''
package com.example.mobile_icon;

import android.content.Intent;
import android.os.Bundle;
import android.os.Handler;
import android.view.View;
import android.widget.ProgressBar;

import androidx.appcompat.app.AppCompatActivity;
import androidx.appcompat.app.AppCompatDelegate;

import java.util.Timer;
import java.util.TimerTask;

public class activitySplash extends AppCompatActivity {
    private static final int SPLASH_TIME_OUT = 10000;
    ProgressBar pb;
    int counter = 0;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_splash);
        prog();

        AppCompatDelegate.setCompatVectorFromResourcesEnabled(true);
        final Handler handler = new Handler();
        handler.postDelayed(() -> {
            startActivity(new Intent(getApplicationContext(), home.class));
            finish();
        }, 10000);

        View decorView = getWindow().getDecorView();
        decorView.setSystemUiVisibility(View.SYSTEM_UI_FLAG_FULLSCREEN);
        if (getSupportActionBar() != null){
            getSupportActionBar().hide();
        }

        new Handler().postDelayed(() -> {
            Intent intent = new Intent(activitySplash.this, home.class);
            startActivity(intent);
            finish();
        }, SPLASH_TIME_OUT);

    }
    public void prog(){
        pb= findViewById(R.id.pb);
        final Timer t = new Timer();
        TimerTask tt=new TimerTask() {
            @Override
            public void run() {
                counter++;
                pb.setProgress(counter);

                if (counter == 100)
                    t.cancel();
            }
        };
        t.schedule(tt,0, 100);
    }
}
'''
B. Code Project Hello World
activity_hello.xml

<?xml version="1.0" encoding="utf-8"?>
@@ -618,7 +646,7 @@ public class HelloActivity extends AppCompatActivity{
}
B. Code Project Count
C. Code Project Count
activity_count.xml

<?xml version="1.0" encoding="utf-8"?>
@@ -849,7 +877,7 @@ public class CountActivity extends AppCompatActivity {
}
C. Code Project Scroll Movie
D. Code Project Scroll Movie
activity_scrollmovie.xml

<?xml version="1.0" encoding="utf-8"?>
@@ -921,7 +949,7 @@ public class SianidaActivity extends AppCompatActivity {
}
Code Project Two Activity
E. Code Project Two Activity
activity_twoactivity.xml
'''
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="@drawable/gb7"
    xmlns:tools="http://schemas.android.com/tools"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    tools:context=".pertamaActivity">

    <TextView
        android:id="@+id/text_header_reply"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="16dp"
        android:layout_marginTop="25dp"
        android:layout_marginEnd="16dp"
        android:textColor="@color/white"
        android:text="@string/text_header_reply"
        android:textAppearance="@style/TextAppearance.AppCompat.Medium"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.498"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <Button
        android:id="@+id/button_main"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="16dp"
        android:layout_marginTop="16dp"
        android:layout_marginEnd="16dp"
        android:onClick="launchSecondActivity"
        android:text="@string/button_main"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.498"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/text_message_reply" />

    <TextView
        android:id="@+id/text_message_reply"
        android:layout_width="0dp"
        android:layout_height="wrap_content"
        android:visibility="visible"
        android:textColor="@color/white"
        app:layout_constraintTop_toBottomOf="@+id/text_header_reply"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        android:layout_marginTop="16dp"
        android:layout_marginStart="16dp"
        android:layout_marginEnd="16dp"/>

    <EditText
        android:id="@+id/editText_main"
        android:layout_width="224dp"
        android:layout_height="66dp"
        android:layout_marginStart="16dp"
        android:layout_marginTop="60dp"
        android:layout_marginEnd="16dp"
        android:textColor="@color/white"
        android:ems="10"
        android:hint="@string/editText_main"
        android:inputType="textLongMessage"
        app:layout_constraintEnd_toEndOf="@id/button_main"
        app:layout_constraintStart_toStartOf="@id/button_main"
        app:layout_constraintTop_toTopOf="@id/button_main" />

</androidx.constraintlayout.widget.ConstraintLayout>

activity_two2activity.xml
'''
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="@drawable/gb6"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    tools:context=".KeduaActivity">

    <TextView
        android:id="@+id/text_header"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/text_header"
        android:textColor="@color/black"
        android:textAppearance="@style/TextAppearance.AppCompat.Medium"
        android:textStyle="bold"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        android:layout_marginTop="20dp"
        android:layout_marginStart="16dp"
        android:layout_marginEnd="16dp"/>

    <EditText
        android:id="@+id/editText_second"
        android:layout_width="0dp"
        android:layout_height="wrap_content"
        android:layout_marginStart="16dp"
        android:layout_marginTop="15dp"
        android:layout_marginEnd="16dp"
        android:ems="10"
        android:textColor="@color/black"
        android:hint="@string/editText_second"
        android:inputType="textLongMessage"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.0"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/text_header" />

    <TextView
        android:id="@+id/text_message"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="16dp"
        app:layout_constraintTop_toBottomOf="@+id/editText_second"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        android:layout_marginStart="16dp"
        android:layout_marginEnd="16dp"/>

    <Button
        android:id="@+id/button_second"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/button_second"
        android:onClick="returnReply"
        app:layout_constraintTop_toBottomOf="@+id/text_message"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        android:layout_marginTop="-30dp"
        android:layout_marginStart="16dp"
        android:layout_marginEnd="0dp"/>

</androidx.constraintlayout.widget.ConstraintLayout>

TwoActivity.java
'''
package com.example.mobile_icon;

import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import android.widget.EditText;
import android.widget.TextView;

import androidx.annotation.Nullable;
import androidx.appcompat.app.AppCompatActivity;

public class pertamaActivity extends AppCompatActivity {

    private static final String LOG_TAG = pertamaActivity.class.getCanonicalName();
    public static final String EXTRA_MESSAGE = "com.example.android.KeduaActivity.extra.MESSAGE";
    public static final int TEXT_REQUEST = 1;
    private EditText mMessageEditText;
    private TextView mReplyHeadTextView;
    private TextView mReplyTextView;

    @Override
    protected void onCreate(@Nullable Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_pertama);

        mMessageEditText = findViewById(R.id.editText_main);
        mReplyHeadTextView = findViewById(R.id.text_header_reply);
        mReplyTextView = findViewById(R.id.text_message_reply);
    }

    public void launchSecondActivity(View view) {
        Intent intent = new Intent(this, KeduaActivity.class);
        startActivity(intent);
    }
}

Two2Activity.java
'''
package com.example.mobile_icon;

import android.content.Intent;
import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;

import androidx.annotation.Nullable;
import androidx.appcompat.app.AppCompatActivity;

public class KeduaActivity extends AppCompatActivity {
    public static final String EXTRA_REPLY = "com.hello.extra.REPLY";
    Button button_second;
    private EditText mReply;

    @Override
    protected void onCreate(@Nullable Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_kedua);

        mReply = findViewById(R.id.editText_second);


        Intent intent = getIntent();
        String message = intent.getStringExtra(pertamaActivity.EXTRA_MESSAGE);

        TextView textView = findViewById(R.id.text_message);
        textView.setText(message);

        button_second = findViewById(R.id.button_second);
        button_second.setOnClickListener(v -> {
            Intent intent1 = new Intent(
                    KeduaActivity.this, pertamaActivity.class
            );
            startActivity(intent1);
        });


    }

    @Override
    public void onBackPressed() {
        Intent replyIntent = new Intent();
        String reply = mReply.getText().toString();
        replyIntent.putExtra(EXTRA_REPLY, reply);
        setResult(RESULT_OK, replyIntent);
        super.onBackPressed();
    }
}
Code Project SetAlarm dan Maps
Pertama, buatlah ikon tombol terlebih dahulu pada activity_main.xml, bersama dengan ikon tombol aplikasi lainnya :
'''
Set Alarm
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="@drawable/gb1"
    tools:context=".SetAlarm">

    <TimePicker
        android:id="@+id/timePicker"
        android:layout_width="403dp"
        android:layout_height="645dp"
        android:numbersTextColor="@color/black"
        android:layout_gravity="center"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <ToggleButton
        android:id="@+id/toggleButton"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_gravity="center"
        android:layout_margin="20dp"
        android:layout_marginTop="28dp"
        android:checked="false"
        android:onClick="OnToggleClicked"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/timePicker" />

</androidx.constraintlayout.widget.ConstraintLayout>
'''
Maps
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="@drawable/gb2"
    android:orientation="vertical"
    tools:context=".MapActivity">

    <TextView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Open google maps"
        android:layout_margin="20dp"
        android:textColor="@color/black"
        android:textStyle="bold"
        android:textSize="30dp"/>

    <androidx.cardview.widget.CardView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        app:cardCornerRadius="10dp"
        app:cardElevation="20dp"
        android:layout_margin="20dp" >

        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="vertical"
            android:layout_margin="10dp">

            <TextView
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="Lokasi awal anda"
                android:textStyle="bold"
                android:textColor="@color/black"
                android:textSize="16sp"/>

            <EditText
                android:id="@+id/etAwal"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:hint="Lokasi awal anda"
                android:minHeight="48dp" />

            <TextView
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="Lokasi tujuan anda"
                android:textColor="@color/black"
                android:textSize="16sp"
                android:textStyle="bold" />

            <EditText
                android:id="@+id/etTujuan"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:hint="Lokasi tujuan anda"
                android:minHeight="48dp" />

            <ImageButton
                android:id="@+id/btnJalur"
                android:layout_width="48dp"
                android:layout_height="48dp"
                android:layout_marginLeft="145dp"
                android:background="@drawable/map" />

        </LinearLayout>

    </androidx.cardview.widget.CardView>

</LinearLayout>
'''
Lalu tambahkan code Implicit Intent pada MainActivity.java :
'''
SetAlarm
package com.example.mobile_icon;

import android.app.AlarmManager;
import android.app.PendingIntent;
import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import android.widget.TimePicker;
import android.widget.Toast;
import android.widget.ToggleButton;

import androidx.appcompat.app.AppCompatActivity;

import java.util.Calendar;

public class SetAlarm extends AppCompatActivity {
    TimePicker alarmTimePicker;
    PendingIntent pendingIntent;
    AlarmManager alarmManager;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_set_alarm);

        alarmTimePicker = findViewById(R.id.timePicker);
        alarmManager = (AlarmManager) getSystemService(ALARM_SERVICE);

    }

    public void OnToggleClicked(View view) {
        long time;
        if (((ToggleButton) view).isChecked()) {
            Toast.makeText(SetAlarm.this, "ALARM ON", Toast.LENGTH_SHORT).show();
            Calendar calendar = Calendar.getInstance();

            calendar.set(Calendar.HOUR_OF_DAY, alarmTimePicker.getHour());
            calendar.set(Calendar.MINUTE, alarmTimePicker.getMinute());

            Intent intent = new Intent(this, AlarmReceiver.class);

            pendingIntent = PendingIntent.getBroadcast(this, 0, intent, PendingIntent.FLAG_IMMUTABLE);

            time = (calendar.getTimeInMillis() - (calendar.getTimeInMillis() % 60000));
            if (System.currentTimeMillis() > time) {

                if (Calendar.AM_PM == 0)
                    time = time + (1000 * 60 * 60 * 12);
                else
                    time = time + (1000 * 60 * 60 * 24);
            }

            alarmManager.setRepeating(AlarmManager.RTC, time, 10000, pendingIntent);

        } else {
            alarmManager.cancel(pendingIntent);
            Toast.makeText(SetAlarm.this, "ALARM OFF", Toast.LENGTH_SHORT).show();
        }
    }
}
'''
Maps
package com.example.mobile_icon;

import android.content.ActivityNotFoundException;
import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.widget.EditText;
import android.widget.ImageButton;

import androidx.appcompat.app.AppCompatActivity;

public class MapActivity extends AppCompatActivity {

    private EditText etAwal, etTujuan;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_map);

        etAwal = findViewById(R.id.etAwal);
        etTujuan = findViewById(R.id.etTujuan);
        ImageButton btnJalur = findViewById(R.id.btnJalur);

        btnJalur.setOnClickListener(view -> {

            String asal = etAwal.getText().toString();
            String tujuan = etTujuan.getText().toString();

            DisplayJalur(asal, tujuan);
        });
    }

    private void DisplayJalur(String asal, String tujuan) {
        try {
            Uri uri = Uri.parse("https://www.google.co.in/maps/dir/" + asal + "/" + tujuan + "?entry=ttu");
            Intent intent = new Intent(Intent.ACTION_VIEW, uri);
            intent.setPackage("com.google.android.apps.maps");
            intent.setFlags(Intent.FLAG_ACTIVITY_NEW_TASK);
            startActivity(intent);
        }catch (ActivityNotFoundException e){
            Uri uri = Uri.parse("https://www.google.com/maps");
            Intent intent = new Intent(Intent.ACTION_VIEW, uri);
            intent.setFlags(Intent.FLAG_ACTIVITY_NEW_TASK);
            startActivity(intent);
        }

    }
}

Selanjutnya buka AndroidManifest.xml dan tambahkan code untuk izin membuka Alarm :

<uses-permission android:name="com.android.alarm.permission.SET_ALARM" />
Tambahkan code berikut pada bagian application agar set alarm dapat berjalan :
'''
<activity
            android:name=".MainActivity"
            android:exported="true">
            <intent-filter>
                <action android:name="android.intent.action.SET_ALARM" />
                <category android:name="android.intent.category.DEFAULT" />
                <action android:name="android.intent.action.VIEW" />
                <data android:scheme="geo" />
                <category android:name="android.intent.category.DEFAULT" />
            </intent-filter>
        </activity>
'''
Hasil Run
Berikut adalah hasil running dari aplikasi yang telah saya buat :
 
https://github.com/firlimaharani/Tgsmobile10/assets/130529482/6f9345bf-a823-4bd1-8ec0-50e9ae23fc1e


Finish, Terima Kasih
