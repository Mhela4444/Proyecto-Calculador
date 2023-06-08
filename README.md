# CalculatorAndroid
Fully functionable calculator app in Android Studio
diseñaremos una calculadora para diseñar una calculadora necesitamos algunos botones para eso crearé un ancho de diseño lineal que coincidirá con la altura principal será ser contenido envuelto y dentro de esto agregaré todos esos botones, así que para el diseño lineal daré la identificación que será el diseño de los botones y la orientación de este diseño lineal lo configuraré en vertical para que este diseño lineal sea un diseño lineal vertical dentro de eso colocará cuatro o cinco diseños lineales, por lo que un diseño lineal más dentro de este ancho coincidirá con la altura principal, se ajustará el contenido será horizontal para que pueda agregar botones en horizontal, así que dentro de esto ahora agregaremos los botone
![image](https://github.com/Mhela4444/Proyecto-Calculador/assets/133244582/7a3d4d83-e1b3-45b3-945e-10ac2ab8353e)

Entonces, para el botón, estoy tomando un botón de material, por lo que usaré el botón de material para que pueda hacer que tenga un ancho circular. 
![image](https://github.com/Mhela4444/Proyecto-Calculador/assets/133244582/4e1a1d56-43e9-47b0-9ceb-ed65bca2ee7a)

Después, debe crear un diseño de superposición especial para mostrar detrás de Circular Revealla vista animada actual. Y para agregar todos los elementos al menú, debe agregarlos todos a LinearLayout
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/solution_tv"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:layout_above="@id/result_tv"
        android:layout_marginStart="16dp"
        android:layout_marginTop="16dp"
        android:layout_marginEnd="16dp"
        android:layout_marginBottom="16dp"
        android:textAlignment="textEnd"
        android:textColor="@color/black"
        android:textSize="32dp" />

    <TextView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:id="@+id/result_tv"
        android:text="0"
        android:textSize="64dp"
        android:textAlignment="textEnd"
        android:textColor="@color/black"
        android:layout_above="@id/buttons_layout"
        android:layout_margin="16dp" />


    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="vertical"
        android:layout_alignParentBottom="true"
        android:background="#F1F1F1"
        android:paddingVertical="16dp"
        android:id="@+id/buttons_layout">

        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:gravity="center"
            android:orientation="horizontal">

            <com.google.android.material.button.MaterialButton
                android:layout_width="72dp"
                android:layout_height="72dp"
                app:cornerRadius="36dp"
                style="@style/Widget.MaterialComponents.ExtendedFloatingActionButton"
                android:textSize="32dp"
                android:textColor="@color/white"
                android:layout_margin="12dp"
                android:id="@+id/button_c"
                android:backgroundTint="#F44336"
                android:text="C" />

            <com.google.android.material.button.MaterialButton
                android:id="@+id/button_open_bracket"
                style="@style/Widget.MaterialComponents.ExtendedFloatingActionButton"
                android:layout_width="72dp"
                android:layout_height="72dp"
                android:layout_margin="12dp"
                android:backgroundTint="#FF9800"
                android:text="("
                android:textColor="@color/white"
                android:textSize="32dp"
                app:cornerRadius="36dp" />

            <com.google.android.material.button.MaterialButton
                android:id="@+id/button_close_bracket"
                style="@style/Widget.MaterialComponents.ExtendedFloatingActionButton"
                android:layout_width="72dp"
                android:layout_height="72dp"
                android:layout_margin="12dp"
                android:backgroundTint="#FF9800"
                android:text=")"
                android:textColor="@color/white"
                android:textSize="32dp"
                app:cornerRadius="36dp" />
            <com.google.android.material.button.MaterialButton
                android:layout_width="72dp"
                android:layout_height="72dp"
                app:cornerRadius="36dp"
                style="@style/Widget.MaterialComponents.ExtendedFloatingActionButton"
                android:textSize="32dp"
                android:textColor="@color/white"
                android:layout_margin="12dp"
                android:id="@+id/button_divide"
                android:backgroundTint="#FF9800"
                android:text="/" />

        </LinearLayout>
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:gravity="center"
            android:orientation="horizontal">

            <com.google.android.material.button.MaterialButton
                android:id="@+id/button_7"
                style="@style/Widget.MaterialComponents.ExtendedFloatingActionButton"
                android:layout_width="72dp"
                android:layout_height="72dp"
                android:layout_margin="12dp"
                android:text="7"
                android:textColor="@color/white"
                android:textSize="32dp"
                app:backgroundTint="#958383"
                app:cornerRadius="36dp" />

            <com.google.android.material.button.MaterialButton
                android:id="@+id/button_8"
                style="@style/Widget.MaterialComponents.ExtendedFloatingActionButton"
                android:layout_width="72dp"
                android:layout_height="72dp"
                android:layout_margin="12dp"
                android:text="8"
                android:textColor="@color/white"
                android:textSize="32dp"
                app:backgroundTint="#958383"
                app:cornerRadius="36dp" />

            <com.google.android.material.button.MaterialButton
                android:id="@+id/button_9"
                style="@style/Widget.MaterialComponents.ExtendedFloatingActionButton"
                android:layout_width="72dp"
                android:layout_height="72dp"
                android:layout_margin="12dp"
                android:text="9"
                android:textColor="@color/white"
                android:textSize="32dp"
                app:backgroundTint="#9F8787"
                app:cornerRadius="36dp" />
            <com.google.android.material.button.MaterialButton
                android:layout_width="72dp"
                android:layout_height="72dp"
                app:cornerRadius="36dp"
                style="@style/Widget.MaterialComponents.ExtendedFloatingActionButton"
                android:textSize="32dp"
                android:textColor="@color/white"
                android:layout_margin="12dp"
                android:id="@+id/button_multiply"
                android:backgroundTint="#FF9800"
                android:text="*" />

        </LinearLayout>
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:gravity="center"
            android:orientation="horizontal">

            <com.google.android.material.button.MaterialButton
                android:id="@+id/button_4"
                style="@style/Widget.MaterialComponents.ExtendedFloatingActionButton"
                android:layout_width="72dp"
                android:layout_height="72dp"
                android:layout_margin="12dp"
                android:text="4"
                android:textColor="@color/white"
                android:textSize="32dp"
                app:backgroundTint="#958383"
                app:cornerRadius="36dp" />

            <com.google.android.material.button.MaterialButton
                android:id="@+id/button_5"
                style="@style/Widget.MaterialComponents.ExtendedFloatingActionButton"
                android:layout_width="72dp"
                android:layout_height="72dp"
                android:layout_margin="12dp"
                android:text="5"
                android:textColor="@color/white"
                android:textSize="32dp"
                app:backgroundTint="#958383"
                app:cornerRadius="36dp" />

            <com.google.android.material.button.MaterialButton
                android:id="@+id/button_6"
                style="@style/Widget.MaterialComponents.ExtendedFloatingActionButton"
                android:layout_width="72dp"
                android:layout_height="72dp"
                android:layout_margin="12dp"
                android:text="6"
                android:textColor="@color/white"
                android:textSize="32dp"
                app:backgroundTint="#958383"
                app:cornerRadius="36dp" />
            <com.google.android.material.button.MaterialButton
                android:layout_width="72dp"
                android:layout_height="72dp"
                app:cornerRadius="36dp"
                style="@style/Widget.MaterialComponents.ExtendedFloatingActionButton"
                android:textSize="32dp"
                android:textColor="@color/white"
                android:layout_margin="12dp"
                android:id="@+id/button_plus"
                android:backgroundTint="#FF9800"
                android:text="+" />

        </LinearLayout>
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:gravity="center"
            android:orientation="horizontal">

            <com.google.android.material.button.MaterialButton
                android:id="@+id/button_1"
                style="@style/Widget.MaterialComponents.ExtendedFloatingActionButton"
                android:layout_width="72dp"
                android:layout_height="72dp"
                android:layout_margin="12dp"
                android:text="1"
                android:textColor="@color/white"
                android:textSize="32dp"
                app:backgroundTint="#958383"
                app:cornerRadius="36dp" />

            <com.google.android.material.button.MaterialButton
                android:id="@+id/button_2"
                style="@style/Widget.MaterialComponents.ExtendedFloatingActionButton"
                android:layout_width="72dp"
                android:layout_height="72dp"
                android:layout_margin="12dp"
                android:text="2"
                android:textColor="@color/white"
                android:textSize="32dp"
                app:backgroundTint="#958383"
                app:cornerRadius="36dp" />

            <com.google.android.material.button.MaterialButton
                android:id="@+id/button_3"
                style="@style/Widget.MaterialComponents.ExtendedFloatingActionButton"
                android:layout_width="72dp"
                android:layout_height="72dp"
                android:layout_margin="12dp"
                android:text="3"
                android:textColor="@color/white"
                android:textSize="32dp"
                app:backgroundTint="#958383"
                app:cornerRadius="36dp" />
            <com.google.android.material.button.MaterialButton
                android:layout_width="72dp"
                android:layout_height="72dp"
                app:cornerRadius="36dp"
                style="@style/Widget.MaterialComponents.ExtendedFloatingActionButton"
                android:textSize="32dp"
                android:textColor="@color/white"
                android:layout_margin="12dp"
                android:id="@+id/button_minus"
                android:backgroundTint="#FF9800"
                android:text="-" />

        </LinearLayout>
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:gravity="center"
            android:orientation="horizontal">

            <com.google.android.material.button.MaterialButton
                android:layout_width="72dp"
                android:layout_height="72dp"
                app:cornerRadius="36dp"
                style="@style/Widget.MaterialComponents.ExtendedFloatingActionButton"
                android:textSize="20dp"
                android:textColor="@color/white"
                android:layout_margin="12dp"
                android:id="@+id/button_ac"
                android:backgroundTint="#F44336"
                android:text="AC" />

            <com.google.android.material.button.MaterialButton
                android:id="@+id/button_0"
                style="@style/Widget.MaterialComponents.ExtendedFloatingActionButton"
                android:layout_width="72dp"
                android:layout_height="72dp"
                android:layout_margin="12dp"
                android:text="0"
                android:textColor="@color/white"
                android:textSize="32dp"
                app:backgroundTint="#958383"
                app:cornerRadius="36dp" />

            <com.google.android.material.button.MaterialButton
                android:id="@+id/button_dot"
                style="@style/Widget.MaterialComponents.ExtendedFloatingActionButton"
                android:layout_width="72dp"
                android:layout_height="72dp"
                android:layout_margin="12dp"
                android:text="."
                android:textColor="@color/white"
                android:textSize="32dp"
                app:backgroundTint="#958383"
                app:cornerRadius="36dp" />
            <com.google.android.material.button.MaterialButton
                android:layout_width="72dp"
                android:layout_height="72dp"
                app:cornerRadius="36dp"
                style="@style/Widget.MaterialComponents.ExtendedFloatingActionButton"
                android:textSize="32dp"
                android:textColor="@color/white"
                android:layout_margin="12dp"
                android:id="@+id/button_equals"
                android:backgroundTint="#FF9800"
                android:text="=" />

        </LinearLayout>

    </LinearLayout>

</RelativeLayout
  
Para la funcionalidad 
  ![image](https://github.com/Mhela4444/Proyecto-Calculador/assets/133244582/6ae893ae-30f4-42d5-b408-8429203bb209)
