# WebView



1) Aggiungere un componente WebView al layout. 
Di seguito le istruzioni per creare una WebView a tutto schermo (match_parent sia per la larghezza che per la lunghezza).
E' importante assegnare un id (nel nostro caso mywebview)  perchè ne avremmo bisogno per richiamarlo dal codice sorgete Kotlin

<WebView
    android:id="@+id/mywebview"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
/>

2) Aggiungere al file di codice Kotlin le seguenti linee.:

val myWebView: WebView = findViewById(R.id.mywebview)
val myurl = "http://www.android.com"
myWebView.loadUrl(myurl)

La prima riga serve per definire l'oggetto myWebView che è di tipo WebView e che è nel layout identificato tramite l'id mywebview
La seconda riga serve per inserire in una costante di tipo stringa la url che si vuole chiamare
La terza riga serve per effettuare la chiamata alla url

Nel nostro esempio la WebView sarà l'unico componente della nostra applicazione e quindi il codice di cui sopra andrà dopo l'onCreate 
del file principale di Kotlin

Da notare inolte che dovremmo importare la classe Webview aggiungendo in testa al codice Kotlin

import android.webkit.WebView

ed inoltre nel Manifest dovremmo aggiungere il permesso per accedere ad internet:

<uses-permission android:name="android.permission.INTERNET" />


