1.-------Client does not support authentication protocol requested by server; consider upgrading MySQL client hatası aldığımda------

              ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '1309'       // wokbench'de çalıştır düzelir.


(Bilgi ) 2. findById yerine artık findByPk kullanılır bilgin olsun.

---------------mmongodb atlas----------
1.)mongo db atlas try free. 
2.) Build your first cluster
3.) Generate database user.
4.) Genereate ip adress.
5.) Connect your application and copy stirng paste to databasee.js.
6.) Download => https://www.mongodb.com/download-center/compass
7.) Connect with MongoDB Compass => Copy the connection string below, and open Compass.exe
8.) You can see database.

------------USING SSL-------------------
1.)enviroment variables yaptık package.json değişiklik yaptık
2.) işimizi kolaylaştıracak şeyler ekledik app.js'e => 
    2.1) helmet => F12 ile incele yaptığında network tabında yapılan isteklerim tüm header'larını görebilirsin.
         compression => assets css dosyaları falan varsa bunları server'da daha küçük yer kaplicak şekilde ayarlıyor.
         morgan => loglama için. istediğimiz bi dosyaya log atabiliyoruz.

3.) SSL => openssl windows yazdık googlewin64OpenSSL pc'ye indirdim kurdum.
4.) konsolda=> openssl req -nodes -new -x509 -keyout server.key -out server.cert => this will give you private key and public key packaged up in a certificate.
    4.1.) çalışmazsa git bash ile çalıştır. dosyanın dizinindeyken            
5.) karşına bilgiler sorular çıkıcak doldur ancak Common Name sorusunu localhost yapmazsan sertifikan çalışmaz. Çünkü domaininin setlemelisin.
6.) proje dizininde server.cert ve servey.key oluştuğunu görüceksin. 
7.) app.js'e https import et artık onu dinle ve projeyi çalıştırdıında artık localhost:3000 açamazsın başına https koyman gerekir.

--------------HEROKU DEPLOY------------
1.) go to heroku log in and create app
2.) heroku login
3.) heroku git:remote -a the-complete-node-with-mongoos
