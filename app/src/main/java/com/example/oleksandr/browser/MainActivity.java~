package com.example.oleksandr.browser;

import android.app.AlertDialog;
import android.app.Dialog;
import android.content.DialogInterface;
import android.os.Bundle;
import android.support.v7.app.AppCompatActivity;
import android.view.Menu;
import android.view.MenuItem;
import android.webkit.WebView;
import android.widget.Toast;

public class MainActivity extends AppCompatActivity {
    private WebView mWevView;
    private MyWebViewClient mMyWebViewClient;
    private Toast mToast;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        mWevView = (WebView) findViewById(R.id.webView);
        mWevView.getSettings().setJavaScriptEnabled(true);
        mWevView.loadUrl("https://www.google.com.ua");
        mWevView.setWebViewClient(new MyWebViewClient());
    }




    @Override
    public boolean onCreateOptionsMenu(Menu menu) {
        getMenuInflater().inflate(R.menu.menu_main, menu);
        return true;
    }

    @Override
    public boolean onOptionsItemSelected(MenuItem item) {
        int id = item.getItemId();



        switch (id){
            case R.id.action_settings:
                final AlertDialog.Builder alertBuilder = new AlertDialog.Builder(MainActivity.this);
                alertBuilder.setTitle("Settings");
                alertBuilder.setMessage("123");
                alertBuilder.setIcon(R.mipmap.ic_launcher);
                alertBuilder.setPositiveButton("Save", new DialogInterface.OnClickListener() {
                    @Override
                    public void onClick(DialogInterface dialog, int which) {
                        //TODO
                    }
                });
                alertBuilder.setNegativeButton("Cancle", new DialogInterface.OnClickListener() {
                    @Override
                    public void onClick(DialogInterface dialog, int which) {
                        //TODO
                    }
                });
                alertBuilder.show();

                break;
            case R.id.back:
                onBackPressed();
                break;
            case R.id.next:
                //TODO
                break;
            case R.id.reload:
                mWevView.reload();
                break;
            default:
                return super.onOptionsItemSelected(item);
        }

        return super.onOptionsItemSelected(item);
    }

    @Override
    public void onBackPressed() {
        if (mWevView.canGoBack()){
            mWevView.goBack();
        }else {
            super.onBackPressed();
            mToast=  Toast.makeText(getApplicationContext(), "The last page", Toast.LENGTH_LONG);
            mToast.show();
        }
    }



}

