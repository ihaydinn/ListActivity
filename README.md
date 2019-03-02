# ListActivity

public class MainActivity extends ListActivity {
 
    String[] aylar = {"Ocak", "Şubat", "Mart", "Nisan", "Mayıs", "Haziran", "Temmuz",
            "Ağustos", "Eylül", "Ekim", "Kasım", "Aralık"};
 
    ListView liste;
 
 
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        liste = getListView();
        ArrayAdapter<String> adapter = new ArrayAdapter<String>
                (this, android.R.layout.simple_list_item_1, aylar);
        liste.setAdapter(adapter);
    }
 
    @Override
    protected void onListItemClick(ListView l, View v, int position, long id) {
        TextView gecici = (TextView) v;
        Toast.makeText(this, position + " " + gecici.getText(), Toast.LENGTH_LONG).show();
    }
}

XML Dosyası

<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/activity_main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:paddingBottom="@dimen/activity_vertical_margin"
    android:paddingLeft="@dimen/activity_horizontal_margin"
    android:paddingRight="@dimen/activity_horizontal_margin"
    android:paddingTop="@dimen/activity_vertical_margin"
    tools:context="ihaydin.com.listactivityornek.MainActivity">
 
    <ListView
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:layout_alignParentTop="true"
        android:id="@android:id/list"
        android:layout_alignParentStart="true" />
</RelativeLayout>

//////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
