<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Haftalık Eğitim Takvimi - 2025</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #2C3E50;
            padding: 20px;
            margin: 0;
            color: #ECF0F1;
        }
        h1 {
            color: #ECF0F1;
            text-align: center;
            font-size: 36px;
            font-weight: bold;
            margin-bottom: 20px;
        }
        h2 {
            color: #2C3E50;
            font-size: 24px;
            font-weight: bold;
            margin-top: 20px;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
            background-color: #fff;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        th, td {
            border: 1px solid #BDC3C7;
            padding: 10px;
            text-align: left;
        }
        th {
            background-color: #3498DB;
            color: white;
        }
        tr:nth-child(even) {
            background-color: #F9E79F;
        }
        tr:hover {
            background-color: #D5F5E3;
            cursor: move;
        }
        tr.dragging {
            opacity: 0.5;
        }
        select, input {
            padding: 5px;
            width: 100%;
            border-radius: 4px;
            border: 1px solid #BDC3C7;
        }
        .yas-6-8 {
            background-color: #A9DFBF;
        }
        .yas-9-12 {
            background-color: #AED6F1;
        }
        button {
            padding: 10px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            margin: 5px;
            color: white;
        }
        .yazdir-btn {
            background-color: #2ECC71;
        }
        .yazdir-btn:hover {
            background-color: #27AE60;
        }
        .pdf-btn {
            background-color: #E74C3C;
        }
        .pdf-btn:hover {
            background-color: #C0392B;
        }
        .rapor-btn {
            background-color: #8E44AD;
        }
        .rapor-btn:hover {
            background-color: #7D3C98;
        }
        .mail-btn {
            background-color: #3498DB;
        }
        .mail-btn:hover {
            background-color: #2980B9;
        }
        .ekle-btn {
            background-color: #F1C40F;
            padding: 5px 10px;
            color: #2C3E50;
            margin-right: 5px;
        }
        .ekle-btn:hover {
            background-color: #D4AC0D;
        }
        .cikar-btn {
            background-color: #E74C3C;
            padding: 5px 10px;
            color: white;
        }
        .cikar-btn:hover {
            background-color: #C0392B;
        }
        .park-section {
            background-color: #fff;
            padding: 20px;
            margin-bottom: 30px;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            color: #2C3E50;
        }
        label {
            color: #2C3E50;
            font-weight: bold;
            margin-right: 10px;
        }
        .secim-alani {
            display: flex;
            gap: 20px;
            margin-bottom: 10px;
        }
        .secim-alani select {
            width: 200px;
        }
        .ozet {
            margin-top: 10px;
            font-weight: bold;
            color: #2C3E50;
        }
        /* Tooltip Stili */
        .tooltip {
            position: relative;
            display: inline-block;
            width: 100%;
        }
        .tooltip .tooltiptext {
            visibility: hidden;
            width: 300px;
            background-color: #555;
            color: #fff;
            text-align: center;
            border-radius: 6px;
            padding: 5px;
            position: absolute;
            z-index: 1;
            bottom: 125%;
            left: 50%;
            margin-left: -150px;
            opacity: 0;
            transition: opacity 0.3s;
        }
        .tooltip:hover .tooltiptext {
            visibility: visible;
            opacity: 1;
        }
    </style>
</head>
<body>
    <h1>Haftalık Eğitim Takvimi - 2025</h1>

    <!-- Topkapı Çocuk Trafik Eğitim Parkı -->
    <div class="park-section">
        <h2>Topkapı Çocuk Trafik Eğitim Parkı</h2>
        <div class="secim-alani">
            <label for="aySecimiTopkapi">Ay Seçimi: </label>
            <select id="aySecimiTopkapi" onchange="haftaGuncelle('Topkapi')">
                <option value="1">Ocak</option>
                <option value="2">Şubat</option>
                <option value="3">Mart</option>
                <option value="4">Nisan</option>
                <option value="5">Mayıs</option>
                <option value="6">Haziran</option>
                <option value="7">Temmuz</option>
                <option value="8">Ağustos</option>
                <option value="9">Eylül</option>
                <option value="10">Ekim</option>
                <option value="11">Kasım</option>
                <option value="12">Aralık</option>
            </select>
            <label for="haftaSecimiTopkapi">Hafta Seçimi: </label>
            <select id="haftaSecimiTopkapi" onchange="veriKaydet('Topkapi')"></select>
        </div>

        <table id="egitimTablosuTopkapi">
            <thead>
                <tr>
                    <th>Gün</th>
                    <th>İlçe</th>
                    <th>Saat</th>
                    <th>Okul Adı</th>
                    <th>Öğrenci Sayısı</th>
                    <th>Okul Türü</th>
                    <th>Yaş Grubu</th>
                    <th>Eğitmen</th>
                    <th>Notlar</th>
                    <th>Okul İletişim Numarası</th>
                    <th>Durum</th>
                    <th>Ekle/Çıkar</th>
                </tr>
            </thead>
            <tbody>
                <tr draggable="true" ondragstart="dragStart(event)" ondragover="dragOver(event)" ondrop="drop(event, 'Topkapi')">
                    <td><select class="gun-select" onchange="veriKaydet('Topkapi')">
                        <option value="Pazartesi" selected>Pazartesi</option>
                        <option value="Salı">Salı</option>
                        <option value="Çarşamba">Çarşamba</option>
                        <option value="Perşembe">Perşembe</option>
                        <option value="Cuma">Cuma</option>
                    </select></td>
                    <td><select>
                        <option value="Adalar">Adalar</option>
                        <option value="Arnavutköy">Arnavutköy</option>
                        <option value="Ataşehir">Ataşehir</option>
                        <option value="Avcılar">Avcılar</option>
                        <option value="Bağcılar">Bağcılar</option>
                        <option value="Bahçelievler">Bahçelievler</option>
                        <option value="Bakırköy">Bakırköy</option>
                        <option value="Başakşehir">Başakşehir</option>
                        <option value="Bayrampaşa">Bayrampaşa</option>
                        <option value="Beşiktaş">Beşiktaş</option>
                        <option value="Beykoz">Beykoz</option>
                        <option value="Beylikdüzü">Beylikdüzü</option>
                        <option value="Beyoğlu">Beyoğlu</option>
                        <option value="Büyükçekmece">Büyükçekmece</option>
                        <option value="Çatalca">Çatalca</option>
                        <option value="Çekmeköy">Çekmeköy</option>
                        <option value="Esenler">Esenler</option>
                        <option value="Esenyurt">Esenyurt</option>
                        <option value="Eyüpsultan">Eyüpsultan</option>
                        <option value="Fatih" selected>Fatih</option>
                        <option value="Gaziosmanpaşa">Gaziosmanpaşa</option>
                        <option value="Güngören">Güngören</option>
                        <option value="Kadıköy">Kadıköy</option>
                        <option value="Kağıthane">Kağıthane</option>
                        <option value="Kartal">Kartal</option>
                        <option value="Küçükçekmece">Küçükçekmece</option>
                        <option value="Maltepe">Maltepe</option>
                        <option value="Pendik">Pendik</option>
                        <option value="Sancaktepe">Sancaktepe</option>
                        <option value="Sarıyer">Sarıyer</option>
                        <option value="Silivri">Silivri</option>
                        <option value="Sultanbeyli">Sultanbeyli</option>
                        <option value="Sultangazi">Sultangazi</option>
                        <option value="Şile">Şile</option>
                        <option value="Şişli">Şişli</option>
                        <option value="Tuzla">Tuzla</option>
                        <option value="Ümraniye">Ümraniye</option>
                        <option value="Üsküdar">Üsküdar</option>
                        <option value="Zeytinburnu">Zeytinburnu</option>
                    </select></td>
                    <td><select>
                        <option value="08:00">08:00</option>
                        <option value="08:30">08:30</option>
                        <option value="09:00" selected>09:00</option>
                        <option value="09:30">09:30</option>
                        <option value="10:00">10:00</option>
                        <option value="10:30">10:30</option>
                        <option value="11:00">11:00</option>
                        <option value="11:30">11:30</option>
                        <option value="12:00">12:00</option>
                        <option value="12:30">12:30</option>
                        <option value="13:00">13:00</option>
                        <option value="13:30">13:30</option>
                        <option value="14:00">14:00</option>
                        <option value="14:30">14:30</option>
                        <option value="15:00">15:00</option>
                    </select></td>
                    <td><input type="text" value="Atatürk İlkokulu"></td>
                    <td><input type="number" value="25" onchange="toplamGuncelle('Topkapi')"></td>
                    <td><select>
                        <option value="Randevu" selected>Randevu</option>
                        <option value="Liste">Liste</option>
                    </select></td>
                    <td><select onchange="renkKodlama(this)">
                        <option value="6-8 Yaş" selected>6-8 Yaş</option>
                        <option value="9-12 Yaş">9-12 Yaş</option>
                    </select></td>
                    <td><select>
                        <option value="" selected>Boş</option>
                        <option value="Ceyda Özgür Avcı">Ceyda Özgür Avcı</option>
                        <option value="Fatma Açıkgöz">Fatma Açıkgöz</option>
                        <option value="Veysel Serkan Butur">Veysel Serkan Butur</option>
                        <option value="Arif Yıldırım">Arif Yıldırım</option>
                    </select></td>
                    <td><div class="tooltip"><input type="text" value="">
                        <span class="tooltiptext">Okulla ilgili oluşan problemler, İETT otobüsleriyle ilgili sorunlar veya başka bir görüş öneri belirtilebilir.</span>
                    </div></td>
                    <td><input type="text" value="" placeholder="Telefon Numarası"></td>
                    <td><select onchange="durumDegistir(this, 'Topkapi')">
                        <option value="Planlandı" selected>Planlandı</option>
                        <option value="Tamamlandı">Tamamlandı</option>
                        <option value="İptal Edildi">İptal Edildi</option>
                        <option value="Yeni Randevu">Yeni Randevu</option>
                    </select></td>
                    <td>
                        <button class="ekle-btn" onclick="yeniSatirEkle('Topkapi')">+</button>
                        <button class="cikar-btn" onclick="satirCikar(this, 'Topkapi')">-</button>
                    </td>
                </tr>
            </tbody>
        </table>
        <div class="ozet" id="ozetTopkapi"></div>
        <button class="yazdir-btn" onclick="yazdir('Topkapi')">Yazdır</button>
        <button class="pdf-btn" onclick="yazdir('Topkapi')">PDF İndir</button>
        <button class="rapor-btn" onclick="raporOlustur('Topkapi')">Rapor Oluştur</button>
        <button class="mail-btn" onclick="mailGonder('Topkapi')">Mail Gönder</button>
    </div>

    <!-- Bağcılar Çocuk Trafik Eğitim Parkı -->
    <div class="park-section">
        <h2>Bağcılar Çocuk Trafik Eğitim Parkı</h2>
        <div class="secim-alani">
            <label for="aySecimiBagcilar">Ay Seçimi: </label>
            <select id="aySecimiBagcilar" onchange="haftaGuncelle('Bagcilar')">
                <option value="1">Ocak</option>
                <option value="2">Şubat</option>
                <option value="3">Mart</option>
                <option value="4">Nisan</option>
                <option value="5">Mayıs</option>
                <option value="6">Haziran</option>
                <option value="7">Temmuz</option>
                <option value="8">Ağustos</option>
                <option value="9">Eylül</option>
                <option value="10">Ekim</option>
                <option value="11">Kasım</option>
                <option value="12">Aralık</option>
            </select>
            <label for="haftaSecimiBagcilar">Hafta Seçimi: </label>
            <select id="haftaSecimiBagcilar" onchange="veriKaydet('Bagcilar')"></select>
        </div>

        <table id="egitimTablosuBagcilar">
            <thead>
                <tr>
                    <th>Gün</th>
                    <th>İlçe</th>
                    <th>Saat</th>
                    <th>Okul Adı</th>
                    <th>Öğrenci Sayısı</th>
                    <th>Okul Türü</th>
                    <th>Yaş Grubu</th>
                    <th>Eğitmen</th>
                    <th>Notlar</th>
                    <th>Okul İletişim Numarası</th>
                    <th>Durum</th>
                    <th>Ekle/Çıkar</th>
                </tr>
            </thead>
            <tbody>
                <tr draggable="true" ondragstart="dragStart(event)" ondragover="dragOver(event)" ondrop="drop(event, 'Bagcilar')">
                    <td><select class="gun-select" onchange="veriKaydet('Bagcilar')">
                        <option value="Pazartesi" selected>Pazartesi</option>
                        <option value="Salı">Salı</option>
                        <option value="Çarşamba">Çarşamba</option>
                        <option value="Perşembe">Perşembe</option>
                        <option value="Cuma">Cuma</option>
                    </select></td>
                    <td><select>
                        <option value="Adalar">Adalar</option>
                        <option value="Arnavutköy">Arnavutköy</option>
                        <option value="Ataşehir">Ataşehir</option>
                        <option value="Avcılar">Avcılar</option>
                        <option value="Bağcılar" selected>Bağcılar</option>
                        <option value="Bahçelievler">Bahçelievler</option>
                        <option value="Bakırköy">Bakırköy</option>
                        <option value="Başakşehir">Başakşehir</option>
                        <option value="Bayrampaşa">Bayrampaşa</option>
                        <option value="Beşiktaş">Beşiktaş</option>
                        <option value="Beykoz">Beykoz</option>
                        <option value="Beylikdüzü">Beylikdüzü</option>
                        <option value="Beyoğlu">Beyoğlu</option>
                        <option value="Büyükçekmece">Büyükçekmece</option>
                        <option value="Çatalca">Çatalca</option>
                        <option value="Çekmeköy">Çekmeköy</option>
                        <option value="Esenler">Esenler</option>
                        <option value="Esenyurt">Esenyurt</option>
                        <option value="Eyüpsultan">Eyüpsultan</option>
                        <option value="Fatih">Fatih</option>
                        <option value="Gaziosmanpaşa">Gaziosmanpaşa</option>
                        <option value="Güngören">Güngören</option>
                        <option value="Kadıköy">Kadıköy</option>
                        <option value="Kağıthane">Kağıthane</option>
                        <option value="Kartal">Kartal</option>
                        <option value="Küçükçekmece">Küçükçekmece</option>
                        <option value="Maltepe">Maltepe</option>
                        <option value="Pendik">Pendik</option>
                        <option value="Sancaktepe">Sancaktepe</option>
                        <option value="Sarıyer">Sarıyer</option>
                        <option value="Silivri">Silivri</option>
                        <option value="Sultanbeyli">Sultanbeyli</option>
                        <option value="Sultangazi">Sultangazi</option>
                        <option value="Şile">Şile</option>
                        <option value="Şişli">Şişli</option>
                        <option value="Tuzla">Tuzla</option>
                        <option value="Ümraniye">Ümraniye</option>
                        <option value="Üsküdar">Üsküdar</option>
                        <option value="Zeytinburnu">Zeytinburnu</option>
                    </select></td>
                    <td><select>
                        <option value="08:00">08:00</option>
                        <option value="08:30">08:30</option>
                        <option value="09:00" selected>09:00</option>
                        <option value="09:30">09:30</option>
                        <option value="10:00">10:00</option>
                        <option value="10:30">10:30</option>
                        <option value="11:00">11:00</option>
                        <option value="11:30">11:30</option>
                        <option value="12:00">12:00</option>
                        <option value="12:30">12:30</option>
                        <option value="13:00">13:00</option>
                        <option value="13:30">13:30</option>
                        <option value="14:00">14:00</option>
                        <option value="14:30">14:30</option>
                        <option value="15:00">15:00</option>
                    </select></td>
                    <td><input type="text" value="Cumhuriyet Lisesi"></td>
                    <td><input type="number" value="30" onchange="toplamGuncelle('Bagcilar')"></td>
                    <td><select>
                        <option value="Randevu">Randevu</option>
                        <option value="Liste" selected>Liste</option>
                    </select></td>
                    <td><select onchange="renkKodlama(this)">
                        <option value="6-8 Yaş">6-8 Yaş</option>
                        <option value="9-12 Yaş" selected>9-12 Yaş</option>
                    </select></td>
                    <td><select>
                        <option value="" selected>Boş</option>
                        <option value="Eser Sultan Bulur">Eser Sultan Bulur</option>
                        <option value="Gülsüm Dinçer">Gülsüm Dinçer</option>
                        <option value="Ali Rıza Kara">Ali Rıza Kara</option>
                        <option value="Ebru Oğuzhan">Ebru Oğuzhan</option>
                    </select></td>
                    <td><div class="tooltip"><input type="text" value="Ders materyalleri hazır">
                        <span class="tooltiptext">Okulla ilgili oluşan problemler, İETT otobüsleriyle ilgili sorunlar veya başka bir görüş öneri belirtilebilir.</span>
                    </div></td>
                    <td><input type="text" value="" placeholder="Telefon Numarası"></td>
                    <td><select onchange="durumDegistir(this, 'Bagcilar')">
                        <option value="Planlandı" selected>Planlandı</option>
                        <option value="Tamamlandı">Tamamlandı</option>
                        <option value="İptal Edildi">İptal Edildi</option>
                        <option value="Yeni Randevu">Yeni Randevu</option>
                    </select></td>
                    <td>
                        <button class="ekle-btn" onclick="yeniSatirEkle('Bagcilar')">+</button>
                        <button class="cikar-btn" onclick="satirCikar(this, 'Bagcilar')">-</button>
                    </td>
                </tr>
            </tbody>
        </table>
        <div class="ozet" id="ozetBagcilar"></div>
        <button class="yazdir-btn" onclick="yazdir('Bagcilar')">Yazdır</button>
        <button class="pdf-btn" onclick="yazdir('Bagcilar')">PDF İndir</button>
        <button class="rapor-btn" onclick="raporOlustur('Bagcilar')">Rapor Oluştur</button>
        <button class="mail-btn" onclick="mailGonder('Bagcilar')">Mail Gönder</button>
    </div>

    <!-- Sancaktepe Çocuk Trafik Eğitim Parkı -->
    <div class="park-section">
        <h2>Sancaktepe Çocuk Trafik Eğitim Parkı</h2>
        <div class="secim-alani">
            <label for="aySecimiSancaktepe">Ay Seçimi: </label>
            <select id="aySecimiSancaktepe" onchange="haftaGuncelle('Sancaktepe')">
                <option value="1">Ocak</option>
                <option value="2">Şubat</option>
                <option value="3">Mart</option>
                <option value="4">Nisan</option>
                <option value="5">Mayıs</option>
                <option value="6">Haziran</option>
                <option value="7">Temmuz</option>
                <option value="8">Ağustos</option>
                <option value="9">Eylül</option>
                <option value="10">Ekim</option>
                <option value="11">Kasım</option>
                <option value="12">Aralık</option>
            </select>
            <label for="haftaSecimiSancaktepe">Hafta Seçimi: </label>
            <select id="haftaSecimiSancaktepe" onchange="veriKaydet('Sancaktepe')"></select>
        </div>

        <table id="egitimTablosuSancaktepe">
            <thead>
                <tr>
                    <th>Gün</th>
                    <th>İlçe</th>
                    <th>Saat</th>
                    <th>Okul Adı</th>
                    <th>Öğrenci Sayısı</th>
                    <th>Okul Türü</th>
                    <th>Yaş Grubu</th>
                    <th>Eğitmen</th>
                    <th>Notlar</th>
                    <th>Okul İletişim Numarası</th>
                    <th>Durum</th>
                    <th>Ekle/Çıkar</th>
                </tr>
            </thead>
            <tbody>
                <tr draggable="true" ondragstart="dragStart(event)" ondragover="dragOver(event)" ondrop="drop(event, 'Sancaktepe')">
                    <td><select class="gun-select" onchange="veriKaydet('Sancaktepe')">
                        <option value="Pazartesi" selected>Pazartesi</option>
                        <option value="Salı">Salı</option>
                        <option value="Çarşamba">Çarşamba</option>
                        <option value="Perşembe">Perşembe</option>
                        <option value="Cuma">Cuma</option>
                    </select></td>
                    <td><select>
                        <option value="Adalar">Adalar</option>
                        <option value="Arnavutköy">Arnavutköy</option>
                        <option value="Ataşehir">Ataşehir</option>
                        <option value="Avcılar">Avcılar</option>
                        <option value="Bağcılar">Bağcılar</option>
                        <option value="Bahçelievler">Bahçelievler</option>
                        <option value="Bakırköy">Bakırköy</option>
                        <option value="Başakşehir">Başakşehir</option>
                        <option value="Bayrampaşa">Bayrampaşa</option>
                        <option value="Beşiktaş">Beşiktaş</option>
                        <option value="Beykoz">Beykoz</option>
                        <option value="Beylikdüzü">Beylikdüzü</option>
                        <option value="Beyoğlu">Beyoğlu</option>
                        <option value="Büyükçekmece">Büyükçekmece</option>
                        <option value="Çatalca">Çatalca</option>
                        <option value="Çekmeköy">Çekmeköy</option>
                        <option value="Esenler">Esenler</option>
                        <option value="Esenyurt">Esenyurt</option>
                        <option value="Eyüpsultan">Eyüpsultan</option>
                        <option value="Fatih">Fatih</option>
                        <option value="Gaziosmanpaşa">Gaziosmanpaşa</option>
                        <option value="Güngören">Güngören</option>
                        <option value="Kadıköy">Kadıköy</option>
                        <option value="Kağıthane">Kağıthane</option>
                        <option value="Kartal">Kartal</option>
                        <option value="Küçükçekmece">Küçükçekmece</option>
                        <option value="Maltepe">Maltepe</option>
                        <option value="Pendik">Pendik</option>
                        <option value="Sancaktepe" selected>Sancaktepe</option>
                        <option value="Sarıyer">Sarıyer</option>
                        <option value="Silivri">Silivri</option>
                        <option value="Sultanbeyli">Sultanbeyli</option>
                        <option value="Sultangazi">Sultangazi</option>
                        <option value="Şile">Şile</option>
                        <option value="Şişli">Şişli</option>
                        <option value="Tuzla">Tuzla</option>
                        <option value="Ümraniye">Ümraniye</option>
                        <option value="Üsküdar">Üsküdar</option>
                        <option value="Zeytinburnu">Zeytinburnu</option>
                    </select></td>
                    <td><select>
                        <option value="08:00">08:00</option>
                        <option value="08:30">08:30</option>
                        <option value="09:00" selected>09:00</option>
                        <option value="09:30">09:30</option>
                        <option value="10:00">10:00</option>
                        <option value="10:30">10:30</option>
                        <option value="11:00">11:00</option>
                        <option value="11:30">11:30</option>
                        <option value="12:00">12:00</option>
                        <option value="12:30">12:30</option>
                        <option value="13:00">13:00</option>
                        <option value="13:30">13:30</option>
                        <option value="14:00">14:00</option>
                        <option value="14:30">14:30</option>
                        <option value="15:00">15:00</option>
                    </select></td>
                    <td><input type="text" value="İnönü Lisesi"></td>
                    <td><input type="number" value="35" onchange="toplamGuncelle('Sancaktepe')"></td>
                    <td><select>
                        <option value="Randevu" selected>Randevu</option>
                        <option value="Liste">Liste</option>
                    </select></td>
                    <td><select onchange="renkKodlama(this)">
                        <option value="6-8 Yaş" selected>6-8 Yaş</option>
                        <option value="9-12 Yaş">9-12 Yaş</option>
                    </select></td>
                    <td><select>
                        <option value="" selected>Boş</option>
                        <option value="Gürkan Avcı">Gürkan Avcı</option>
                        <option value="Muhammed Emin Aksoy">Muhammed Emin Aksoy</option>
                        <option value="Tuğba Özcan">Tuğba Özcan</option>
                        <option value="Zehra Çakır">Zehra Çakır</option>
                    </select></td>
                    <td><div class="tooltip"><input type="text" value="">
                        <span class="tooltiptext">Okulla ilgili oluşan problemler, İETT otobüsleriyle ilgili sorunlar veya başka bir görüş öneri belirtilebilir.</span>
                    </div></td>
                    <td><input type="text" value="" placeholder="Telefon Numarası"></td>
                    <td><select onchange="durumDegistir(this, 'Sancaktepe')">
                        <option value="Planlandı" selected>Planlandı</option>
                        <option value="Tamamlandı">Tamamlandı</option>
                        <option value="İptal Edildi">İptal Edildi</option>
                        <option value="Yeni Randevu">Yeni Randevu</option>
                    </select></td>
                    <td>
                        <button class="ekle-btn" onclick="yeniSatirEkle('Sancaktepe')">+</button>
                        <button class="cikar-btn" onclick="satirCikar(this, 'Sancaktepe')">-</button>
                    </td>
                </tr>
            </tbody>
        </table>
        <div class="ozet" id="ozetSancaktepe"></div>
        <button class="yazdir-btn" onclick="yazdir('Sancaktepe')">Yazdır</button>
        <button class="pdf-btn" onclick="yazdir('Sancaktepe')">PDF İndir</button>
        <button class="rapor-btn" onclick="raporOlustur('Sancaktepe')">Rapor Oluştur</button>
        <button class="mail-btn" onclick="mailGonder('Sancaktepe')">Mail Gönder</button>
    </div>

    <!-- JavaScript -->
    <script>
        let draggedRow = null;

        // WhatsApp grup ID'si (burayı ilgili grup ID ile güncelleyin)
        const whatsappGroupId = "YOUR_WHATSAPP_GROUP_ID_HERE"; // WhatsApp grup ID'sini buraya ekleyin

        // Sürükleme Başlangıcı
        function dragStart(event) {
            draggedRow = event.target;
            event.dataTransfer.effectAllowed = "move";
            draggedRow.classList.add("dragging");
        }

        // Sürükleme Üzerinde
        function dragOver(event) {
            event.preventDefault();
            event.dataTransfer.dropEffect = "move";
        }

        // Bırakma
        function drop(event, park) {
            event.preventDefault();
            const targetRow = event.target.closest("tr");
            if (targetRow && draggedRow !== targetRow) {
                const tbody = document.getElementById(`egitimTablosu${park}`).getElementsByTagName("tbody")[0];
                const rows = Array.from(tbody.getElementsByTagName("tr"));
                const draggedIndex = rows.indexOf(draggedRow);
                const targetIndex = rows.indexOf(targetRow);

                if (draggedIndex < targetIndex) {
                    targetRow.parentNode.insertBefore(draggedRow, targetRow.nextSibling);
                } else {
                    targetRow.parentNode.insertBefore(draggedRow, targetRow);
                }
            }
            draggedRow.classList.remove("dragging");
            draggedRow = null;
            veriKaydet(park);
        }

        // Hafta Seçimi Güncelleme
        function haftaGuncelle(park) {
            const ay = parseInt(document.getElementById(`aySecimi${park}`).value);
            const haftaSecimi = document.getElementById(`haftaSecimi${park}`);
            haftaSecimi.innerHTML = "";

            const haftalar = {
                1: ["6-10 Ocak 2025", "13-17 Ocak 2025", "20-24 Ocak 2025", "27-31 Ocak 2025"],
                2: ["3-7 Şubat 2025", "10-14 Şubat 2025", "17-21 Şubat 2025", "24-28 Şubat 2025"],
                3: ["3-7 Mart 2025", "10-14 Mart 2025", "17-21 Mart 2025", "24-28 Mart 2025", "31 Mart-4 Nisan 2025"],
                4: ["7-11 Nisan 2025", "14-18 Nisan 2025", "21-25 Nisan 2025", "28 Nisan-2 Mayıs 2025"],
                5: ["5-9 Mayıs 2025", "12-16 Mayıs 2025", "19-23 Mayıs 2025", "26-30 Mayıs 2025"],
                6: ["2-6 Haziran 2025", "9-13 Haziran 2025", "16-20 Haziran 2025", "23-27 Haziran 2025", "30 Haziran-4 Temmuz 2025"],
                7: ["7-11 Temmuz 2025", "14-18 Temmuz 2025", "21-25 Temmuz 2025", "28 Temmuz-1 Ağustos 2025"],
                8: ["4-8 Ağustos 2025", "11-15 Ağustos 2025", "18-22 Ağustos 2025", "25-29 Ağustos 2025"],
                9: ["1-5 Eylül 2025", "8-12 Eylül 2025", "15-19 Eylül 2025", "22-26 Eylül 2025", "29 Eylül-3 Ekim 2025"],
                10: ["6-10 Ekim 2025", "13-17 Ekim 2025", "20-24 Ekim 2025", "27-31 Ekim 2025"],
                11: ["3-7 Kasım 2025", "10-14 Kasım 2025", "17-21 Kasım 2025", "24-28 Kasım 2025"],
                12: ["1-5 Aralık 2025", "8-12 Aralık 2025", "15-19 Aralık 2025", "22-26 Aralık 2025", "29 Aralık-2 Ocak 2026"]
            };

            const secilenAyHaftalari = haftalar[ay] || [];
            secilenAyHaftalari.forEach(hafta => {
                const option = document.createElement("option");
                option.value = hafta;
                option.text = hafta;
                haftaSecimi.appendChild(option);
            });

            if (secilenAyHaftalari.length > 0) {
                haftaSecimi.value = secilenAyHaftalari[0];
                veriKaydet(park);
            }
        }

        // Renk Kodlaması
        function renkKodlama(yasSelect) {
            const row = yasSelect.parentElement.parentElement;
            row.classList.remove("yas-6-8", "yas-9-12");
            if (yasSelect.value === "6-8 Yaş") row.classList.add("yas-6-8");
            if (yasSelect.value === "9-12 Yaş") row.classList.add("yas-9-12");
        }

        // Saat Sıralama
        function saatSirala(park) {
            const tbody = document.getElementById(`egitimTablosu${park}`).getElementsByTagName("tbody")[0];
            const rows = Array.from(tbody.getElementsByTagName("tr"));

            rows.sort((a, b) => {
                const saatA = a.querySelector("td:nth-child(3) select").value;
                const saatB = b.querySelector("td:nth-child(3) select").value;
                return saatA.localeCompare(saatB);
            });

            rows.forEach(row => tbody.appendChild(row));
        }

        // Yeni Satır Ekleme
        function yeniSatirEkle(park) {
            const tbody = document.getElementById(`egitimTablosu${park}`).getElementsByTagName("tbody")[0];
            const yeniSatir = document.createElement("tr");
            const eğitmenler = {
                Topkapi: ["Ceyda Özgür Avcı", "Fatma Açıkgöz", "Veysel Serkan Butur", "Arif Yıldırım"],
                Bagcilar: ["Eser Sultan Bulur", "Gülsüm Dinçer", "Ali Rıza Kara", "Ebru Oğuzhan"],
                Sancaktepe: ["Gürkan Avcı", "Muhammed Emin Aksoy", "Tuğba Özcan", "Zehra Çakır"]
            };

            yeniSatir.draggable = true;
            yeniSatir.ondragstart = (event) => dragStart(event);
            yeniSatir.ondragover = (event) => dragOver(event);
            yeniSatir.ondrop = (event) => drop(event, park);

            yeniSatir.innerHTML = `
                <td><select class="gun-select" onchange="veriKaydet('${park}')">
                    <option value="Pazartesi">Pazartesi</option>
                    <option value="Salı">Salı</option>
                    <option value="Çarşamba">Çarşamba</option>
                    <option value="Perşembe">Perşembe</option>
                    <option value="Cuma">Cuma</option>
                </select></td>
                <td><select>
                    <option value="Adalar">Adalar</option>
                    <option value="Arnavutköy">Arnavutköy</option>
                    <option value="Ataşehir">Ataşehir</option>
                    <option value="Avcılar">Avcılar</option>
                    <option value="Bağcılar">Bağcılar</option>
                    <option value="Bahçelievler">Bahçelievler</option>
                    <option value="Bakırköy">Bakırköy</option>
                    <option value="Başakşehir">Başakşehir</option>
                    <option value="Bayrampaşa">Bayrampaşa</option>
                    <option value="Beşiktaş">Beşiktaş</option>
                    <option value="Beykoz">Beykoz</option>
                    <option value="Beylikdüzü">Beylikdüzü</option>
                    <option value="Beyoğlu">Beyoğlu</option>
                    <option value="Büyükçekmece">Büyükçekmece</option>
                    <option value="Çatalca">Çatalca</option>
                    <option value="Çekmeköy">Çekmeköy</option>
                    <option value="Esenler">Esenler</option>
                    <option value="Esenyurt">Esenyurt</option>
                    <option value="Eyüpsultan">Eyüpsultan</option>
                    <option value="Fatih">Fatih</option>
                    <option value="Gaziosmanpaşa">Gaziosmanpaşa</option>
                    <option value="Güngören">Güngören</option>
                    <option value="Kadıköy">Kadıköy</option>
                    <option value="Kağıthane">Kağıthane</option>
                    <option value="Kartal">Kartal</option>
                    <option value="Küçükçekmece">Küçükçekmece</option>
                    <option value="Maltepe">Maltepe</option>
                    <option value="Pendik">Pendik</option>
                    <option value="Sancaktepe">Sancaktepe</option>
                    <option value="Sarıyer">Sarıyer</option>
                    <option value="Silivri">Silivri</option>
                    <option value="Sultanbeyli">Sultanbeyli</option>
                    <option value="Sultangazi">Sultangazi</option>
                    <option value="Şile">Şile</option>
                    <option value="Şişli">Şişli</option>
                    <option value="Tuzla">Tuzla</option>
                    <option value="Ümraniye">Ümraniye</option>
                    <option value="Üsküdar">Üsküdar</option>
                    <option value="Zeytinburnu">Zeytinburnu</option>
                </select></td>
                <td><select>
                    <option value="08:00">08:00</option>
                    <option value="08:30">08:30</option>
                    <option value="09:00">09:00</option>
                    <option value="09:30">09:30</option>
                    <option value="10:00">10:00</option>
                    <option value="10:30">10:30</option>
                    <option value="11:00">11:00</option>
                    <option value="11:30">11:30</option>
                    <option value="12:00">12:00</option>
                    <option value="12:30">12:30</option>
                    <option value="13:00">13:00</option>
                    <option value="13:30">13:30</option>
                    <option value="14:00">14:00</option>
                    <option value="14:30">14:30</option>
                    <option value="15:00">15:00</option>
                </select></td>
                <td><input type="text" value=""></td>
                <td><input type="number" value="0" onchange="toplamGuncelle('${park}')"></td>
                <td><select>
                    <option value="Randevu">Randevu</option>
                    <option value="Liste">Liste</option>
                </select></td>
                <td><select onchange="renkKodlama(this)">
                    <option value="6-8 Yaş">6-8 Yaş</option>
                    <option value="9-12 Yaş">9-12 Yaş</option>
                </select></td>
                <td><select>
                    <option value="" selected>Boş</option>
                    ${eğitmenler[park].map(e => `<option value="${e}">${e}</option>`).join('')}
                </select></td>
                <td><div class="tooltip"><input type="text" value="">
                    <span class="tooltiptext">Okulla ilgili oluşan problemler, İETT otobüsleriyle ilgili sorunlar veya başka bir görüş öneri belirtilebilir.</span>
                </div></td>
                <td><input type="text" value="" placeholder="Telefon Numarası"></td>
                <td><select onchange="durumDegistir(this, '${park}')">
                    <option value="Planlandı">Planlandı</option>
                    <option value="Tamamlandı">Tamamlandı</option>
                    <option value="İptal Edildi">İptal Edildi</option>
                    <option value="Yeni Randevu">Yeni Randevu</option>
                </select></td>
                <td>
                    <button class="ekle-btn" onclick="yeniSatirEkle('${park}')">+</button>
                    <button class="cikar-btn" onclick="satirCikar(this, '${park}')">-</button>
                </td>
            `;
            tbody.appendChild(yeniSatir);
            saatSirala(park);
            toplamGuncelle(park);
            veriKaydet(park);
        }

        // Satır Çıkarma
        function satirCikar(button, park) {
            const row = button.parentElement.parentElement;
            row.remove();
            saatSirala(park);
            toplamGuncelle(park);
            veriKaydet(park);
        }

        // Durum Değiştirme ve WhatsApp Gönderme
        function durumDegistir(select, park) {
            const row = select.parentElement.parentElement;
            const durum = select.value;
            if (durum === "İptal Edildi" || durum === "Yeni Randevu") {
                const gun = row.querySelector(".gun-select").value;
                const ilce = row.querySelector("td:nth-child(2) select").value;
                const saat = row.querySelector("td:nth-child(3) select").value;
                const okul = row.querySelector("td:nth-child(4) input").value;
                let mesaj = "";
                if (durum === "İptal Edildi") {
                    mesaj = `${park} - ${gun} ${saat} tarihinde ${ilce} ilçesindeki ${okul} için planlanan eğitim iptal edilmiştir.`;
                } else if (durum === "Yeni Randevu") {
                    mesaj = `${park} - ${gun} ${saat} tarihinde ${ilce} ilçesindeki ${okul} için yeni bir randevu oluşturulmuştur.`;
                }
                window.open(`https://api.whatsapp.com/send?phone=${whatsappGroupId}&text=${encodeURIComponent(mesaj)}`, '_blank');
            }
            toplamGuncelle(park);
            veriKaydet(park);
        }

        // Toplamları Güncelle
        function toplamGuncelle(park) {
            const tbody = document.getElementById(`egitimTablosu${park}`).getElementsByTagName("tbody")[0];
            const rows = tbody.getElementsByTagName("tr");
            let toplamOgrenci = 0;
            let toplamEgitim = 0;

            for (let row of rows) {
                const ogrenciSayisi = parseInt(row.querySelector("td:nth-child(5) input").value) || 0;
                const durum = row.querySelector("td:nth-child(11) select").value;
                if (durum !== "İptal Edildi") {
                    toplamOgrenci += ogrenciSayisi;
                    toplamEgitim++;
                }
            }

            document.getElementById(`ozet${park}`).innerHTML = `Toplam Öğrenci Sayısı: ${toplamOgrenci} | Toplam Eğitim Sayısı: ${toplamEgitim}`;
            veriKaydet(park);
        }

        // Veri Kaydetme
        function veriKaydet(park) {
            const tbody = document.getElementById(`egitimTablosu${park}`).getElementsByTagName("tbody")[0];
            const rows = tbody.getElementsByTagName("tr");
            const haftaSecimi = document.getElementById(`haftaSecimi${park}`).value;
            const veri = [];

            for (let row of rows) {
                const satir = {
                    hafta: haftaSecimi,
                    gun: row.querySelector(".gun-select").value,
                    ilce: row.querySelector("td:nth-child(2) select").value,
                    saat: row.querySelector("td:nth-child(3) select").value,
                    okul: row.querySelector("td:nth-child(4) input").value,
                    ogrenci: row.querySelector("td:nth-child(5) input").value,
                    tur: row.querySelector("td:nth-child(6) select").value,
                    yas: row.querySelector("td:nth-child(7) select").value,
                    egitmen: row.querySelector("td:nth-child(8) select").value,
                    notlar: row.querySelector("td:nth-child(9) input").value,
                    iletisimNumarasi: row.querySelector("td:nth-child(10) input").value,
                    durum: row.querySelector("td:nth-child(11) select").value
                };
                veri.push(satir);
            }
            localStorage.setItem(`egitimTablosu${park}`, JSON.stringify(veri));
        }

        // Veri Yükleme
        function veriYukle(park) {
            const veri = JSON.parse(localStorage.getItem(`egitimTablosu${park}`));
            if (veri && veri.length > 0) {
                const tbody = document.getElementById(`egitimTablosu${park}`).getElementsByTagName("tbody")[0];
                tbody.innerHTML = "";
                veri.forEach(satir => {
                    const yeniSatir = document.createElement("tr");
                    const eğitmenler = {
                        Topkapi: ["Ceyda Özgür Avcı", "Fatma Açıkgöz", "Veysel Serkan Butur", "Arif Yıldırım"],
                        Bagcilar: ["Eser Sultan Bulur", "Gülsüm Dinçer", "Ali Rıza Kara", "Ebru Oğuzhan"],
                        Sancaktepe: ["Gürkan Avcı", "Muhammed Emin Aksoy", "Tuğba Özcan", "Zehra Çakır"]
                    };

                    yeniSatir.draggable = true;
                    yeniSatir.ondragstart = (event) => dragStart(event);
                    yeniSatir.ondragover = (event) => dragOver(event);
                    yeniSatir.ondrop = (event) => drop(event, park);

                    yeniSatir.innerHTML = `
                        <td><select class="gun-select" onchange="veriKaydet('${park}')">
                            <option value="Pazartesi" ${satir.gun === "Pazartesi" ? "selected" : ""}>Pazartesi</option>
                            <option value="Salı" ${satir.gun === "Salı" ? "selected" : ""}>Salı</option>
                            <option value="Çarşamba" ${satir.gun === "Çarşamba" ? "selected" : ""}>Çarşamba</option>
                            <option value="Perşembe" ${satir.gun === "Perşembe" ? "selected" : ""}>Perşembe</option>
                            <option value="Cuma" ${satir.gun === "Cuma" ? "selected" : ""}>Cuma</option>
                        </select></td>
                        <td><select>
                            <option value="Adalar" ${satir.ilce === "Adalar" ? "selected" : ""}>Adalar</option>
                            <option value="Arnavutköy" ${satir.ilce === "Arnavutköy" ? "selected" : ""}>Arnavutköy</option>
                            <option value="Ataşehir" ${satir.ilce === "Ataşehir" ? "selected" : ""}>Ataşehir</option>
                            <option value="Avcılar" ${satir.ilce === "Avcılar" ? "selected" : ""}>Avcılar</option>
                            <option value="Bağcılar" ${satir.ilce === "Bağcılar" ? "selected" : ""}>Bağcılar</option>
                            <option value="Bahçelievler" ${satir.ilce === "Bahçelievler" ? "selected" : ""}>Bahçelievler</option>
                            <option value="Bakırköy" ${satir.ilce === "Bakırköy" ? "selected" : ""}>Bakırköy</option>
                            <option value="Başakşehir" ${satir.ilce === "Başakşehir" ? "selected" : ""}>Başakşehir</option>
                            <option value="Bayrampaşa" ${satir.ilce === "Bayrampaşa" ? "selected" : ""}>Bayrampaşa</option>
                            <option value="Beşiktaş" ${satir.ilce === "Beşiktaş" ? "selected" : ""}>Beşiktaş</option>
                            <option value="Beykoz" ${satir.ilce === "Beykoz" ? "selected" : ""}>Beykoz</option>
                            <option value="Beylikdüzü" ${satir.ilce === "Beylikdüzü" ? "selected" : ""}>Beylikdüzü</option>
                            <option value="Beyoğlu" ${satir.ilce === "Beyoğlu" ? "selected" : ""}>Beyoğlu</option>
                            <option value="Büyükçekmece" ${satir.ilce === "Büyükçekmece" ? "selected" : ""}>Büyükçekmece</option>
                            <option value="Çatalca" ${satir.ilce === "Çatalca" ? "selected" : ""}>Çatalca</option>
                            <option value="Çekmeköy" ${satir.ilce === "Çekmeköy" ? "selected" : ""}>Çekmeköy</option>
                            <option value="Esenler" ${satir.ilce === "Esenler" ? "selected" : ""}>Esenler</option>
                            <option value="Esenyurt" ${satir.ilce === "Esenyurt" ? "selected" : ""}>Esenyurt</option>
                            <option value="Eyüpsultan" ${satir.ilce === "Eyüpsultan" ? "selected" : ""}>Eyüpsultan</option>
                            <option value="Fatih" ${satir.ilce === "Fatih" ? "selected" : ""}>Fatih</option>
                            <option value="Gaziosmanpaşa" ${satir.ilce === "Gaziosmanpaşa" ? "selected" : ""}>Gaziosmanpaşa</option>
                            <option value="Güngören" ${satir.ilce === "Güngören" ? "selected" : ""}>Güngören</option>
                            <option value="Kadıköy" ${satir.ilce === "Kadıköy" ? "selected" : ""}>Kadıköy</option>
                            <option value="Kağıthane" ${satir.ilce === "Kağıthane" ? "selected" : ""}>Kağıthane</option>
                            <option value="Kartal" ${satir.ilce === "Kartal" ? "selected" : ""}>Kartal</option>
                            <option value="Küçükçekmece" ${satir.ilce === "Küçükçekmece" ? "selected" : ""}>Küçükçekmece</option>
                            <option value="Maltepe" ${satir.ilce === "Maltepe" ? "selected" : ""}>Maltepe</option>
                            <option value="Pendik" ${satir.ilce === "Pendik" ? "selected" : ""}>Pendik</option>
                            <option value="Sancaktepe" ${satir.ilce === "Sancaktepe" ? "selected" : ""}>Sancaktepe</option>
                            <option value="Sarıyer" ${satir.ilce === "Sarıyer" ? "selected" : ""}>Sarıyer</option>
                            <option value="Silivri" ${satir.ilce === "Silivri" ? "selected" : ""}>Silivri</option>
                            <option value="Sultanbeyli" ${satir.ilce === "Sultanbeyli" ? "selected" : ""}>Sultanbeyli</option>
                            <option value="Sultangazi" ${satir.ilce === "Sultangazi" ? "selected" : ""}>Sultangazi</option>
                            <option value="Şile" ${satir.ilce === "Şile" ? "selected" : ""}>Şile</option>
                            <option value="Şişli" ${satir.ilce === "Şişli" ? "selected" : ""}>Şişli</option>
                            <option value="Tuzla" ${satir.ilce === "Tuzla" ? "selected" : ""}>Tuzla</option>
                            <option value="Ümraniye" ${satir.ilce === "Ümraniye" ? "selected" : ""}>Ümraniye</option>
                            <option value="Üsküdar" ${satir.ilce === "Üsküdar" ? "selected" : ""}>Üsküdar</option>
                            <option value="Zeytinburnu" ${satir.ilce === "Zeytinburnu" ? "selected" : ""}>Zeytinburnu</option>
                        </select></td>
                        <td><select>
                            <option value="08:00" ${satir.saat === "08:00" ? "selected" : ""}>08:00</option>
                            <option value="08:30" ${satir.saat === "08:30" ? "selected" : ""}>08:30</option>
                            <option value="09:00" ${satir.saat === "09:00" ? "selected" : ""}>09:00</option>
                            <option value="09:30" ${satir.saat === "09:30" ? "selected" : ""}>09:30</option>
                            <option value="10:00" ${satir.saat === "10:00" ? "selected" : ""}>10:00</option>
                            <option value="10:30" ${satir.saat === "10:30" ? "selected" : ""}>10:30</option>
                            <option value="11:00" ${satir.saat === "11:00" ? "selected" : ""}>11:00</option>
                            <option value="11:30" ${satir.saat === "11:30" ? "selected" : ""}>11:30</option>
                            <option value="12:00" ${satir.saat === "12:00" ? "selected" : ""}>12:00</option>
                            <option value="12:30" ${satir.saat === "12:30" ? "selected" : ""}>12:30</option>
                            <option value="13:00" ${satir.saat === "13:00" ? "selected" : ""}>13:00</option>
                            <option value="13:30" ${satir.saat === "13:30" ? "selected" : ""}>13:30</option>
                            <option value="14:00" ${satir.saat === "14:00" ? "selected" : ""}>14:00</option>
                            <option value="14:30" ${satir.saat === "14:30" ? "selected" : ""}>14:30</option>
                            <option value="15:00" ${satir.saat === "15:00" ? "selected" : ""}>15:00</option>
                        </select></td>
                        <td><input type="text" value="${satir.okul}"></td>
                        <td><input type="number" value="${satir.ogrenci}" onchange="toplamGuncelle('${park}')"></td>
                        <td><select>
                            <option value="Randevu" ${satir.tur === "Randevu" ? "selected" : ""}>Randevu</option>
                            <option value="Liste" ${satir.tur === "Liste" ? "selected" : ""}>Liste</option>
                        </select></td>
                        <td><select onchange="renkKodlama(this)">
                            <option value="6-8 Yaş" ${satir.yas === "6-8 Yaş" ? "selected" : ""}>6-8 Yaş</option>
                            <option value="9-12 Yaş" ${satir.yas === "9-12 Yaş" ? "selected" : ""}>9-12 Yaş</option>
                        </select></td>
                        <td><select>
                            <option value="" ${satir.egitmen === "" ? "selected" : ""}>Boş</option>
                            ${eğitmenler[park].map(e => `<option value="${e}" ${satir.egitmen === e ? "selected" : ""}>${e}</option>`).join('')}
                        </select></td>
                        <td><div class="tooltip"><input type="text" value="${satir.notlar}">
                            <span class="tooltiptext">Okulla ilgili oluşan problemler, İETT otobüsleriyle ilgili sorunlar veya başka bir görüş öneri belirtilebilir.</span>
                        </div></td>
                        <td><input type="text" value="${satir.iletisimNumarasi || ''}" placeholder="Telefon Numarası"></td>
                        <td><select onchange="durumDegistir(this, '${park}')">
                            <option value="Planlandı" ${satir.durum === "Planlandı" ? "selected" : ""}>Planlandı</option>
                            <option value="Tamamlandı" ${satir.durum === "Tamamlandı" ? "selected" : ""}>Tamamlandı</option>
                            <option value="İptal Edildi" ${satir.durum === "İptal Edildi" ? "selected" : ""}>İptal Edildi</option>
                            <option value="Yeni Randevu" ${satir.durum === "Yeni Randevu" ? "selected" : ""}>Yeni Randevu</option>
                        </select></td>
                        <td>
                            <button class="ekle-btn" onclick="yeniSatirEkle('${park}')">+</button>
                            <button class="cikar-btn" onclick="satirCikar(this, '${park}')">-</button>
                        </td>
                    `;
                    tbody.appendChild(yeniSatir);
                });
            }
            saatSirala(park);
            toplamGuncelle(park);
        }

        // Yazdır ve PDF İndir
        function yazdir(park) {
            const table = document.getElementById(`egitimTablosu${park}`);
            const rows = table.getElementsByTagName("tr");
            let tableHTML = '<table border="1" style="border-collapse: collapse; width: 100%;">';
            
            const headers = table.querySelectorAll("th");
            tableHTML += '<tr>';
            for (let header of headers) {
                if (header.textContent !== "Ekle/Çıkar") {
                    tableHTML += `<th style="background-color: #3498DB; color: white; padding: 10px;">${header.textContent}</th>`;
                }
            }
            tableHTML += '</tr>';

            for (let row of rows) {
                if (row.parentElement.tagName === "TBODY") {
                    tableHTML += '<tr>';
                    const cells = row.getElementsByTagName("td");
                    for (let i = 0; i < cells.length - 1; i++) {
                        const cell = cells[i];
                        const input = cell.querySelector("input");
                        const select = cell.querySelector("select");
                        let value = "";
                        if (input) value = input.value;
                        else if (select) value = select.options[select.selectedIndex].text;
                        tableHTML += `<td style="padding: 10px;">${value}</td>`;
                    }
                    tableHTML += '</tr>';
                }
            }
            tableHTML += '</table>';

            const win = window.open('', '', 'height=500,width=800');
            win.document.write('<html><head><title>Eğitim Takvimi</title>');
            win.document.write('<style>table { border-collapse: collapse; width: 100%; } th, td { border: 1px solid #BDC3C7; padding: 10px; text-align: left; }</style>');
            win.document.write('</head><body>');
            win.document.write(`<h2>${park} Çocuk Trafik Eğitim Parkı</h2>`);
            win.document.write(tableHTML);
            win.document.write('</body></html>');
            win.document.close();
            win.print();
        }

        // Rapor Oluştur
        function raporOlustur(park) {
            const tbody = document.getElementById(`egitimTablosu${park}`).getElementsByTagName("tbody")[0];
            const rows = tbody.getElementsByTagName("tr");
            const egitmenRaporu = {};
            let toplamOgrenci = 0;

            for (let row of rows) {
                const egitmen = row.querySelector("td:nth-child(8) select").value;
                const ogrenciSayisi = parseInt(row.querySelector("td:nth-child(5) input").value) || 0;
                const durum = row.querySelector("td:nth-child(11) select").value;
                if (durum === "Planlandı" || durum === "Tamamlandı" || durum === "Yeni Randevu") {
                    egitmenRaporu[egitmen] = (egitmenRaporu[egitmen] || 0) + 1;
                    toplamOgrenci += ogrenciSayisi;
                }
            }

            const win = window.open('', '', 'height=500,width=800');
            win.document.write('<html><head><title>Rapor</title>');
            win.document.write('<style>body { font-family: Arial, sans-serif; } h2 { font-size: 20px; } p { font-size: 14px; margin: 5px 0; }</style>');
            win.document.write('</head><body>');
            win.document.write(`<h2>${park} Çocuk Trafik Eğitim Parkı - Rapor</h2>`);
            win.document.write(`<p>Toplam Öğrenci Sayısı: ${toplamOgrenci}</p>`);
            win.document.write('<p>Eğitmen Ders Dağılımı:</p>');
            for (let egitmen in egitmenRaporu) {
                win.document.write(`<p>${egitmen}: ${egitmenRaporu[egitmen]} ders</p>`);
            }
            win.document.write('</body></html>');
            win.document.close();
            win.print();
        }

        // Mail Gönder (Düzenli Tablo)
        function mailGonder(park) {
            const table = document.getElementById(`egitimTablosu${park}`);
            const rows = table.getElementsByTagName("tr");
            const haftaSecimi = document.getElementById(`haftaSecimi${park}`).value;
            let tableText = `${park} Çocuk Trafik Eğitim Parkı Takvimi - Hafta: ${haftaSecimi}nn`;

            // Başlık Satırı
            const headers = table.querySelectorAll("th");
            let headerLine = "|";
            for (let header of headers) {
                if (header.textContent !== "Ekle/Çıkar") {
                    headerLine += ` ${header.textContent.padEnd(15)} |`;
                }
            }
            tableText += headerLine + "n";
            tableText += "|".padEnd(headerLine.length, "-") + "|n";

            // Veri Satırları
            for (let row of rows) {
                if (row.parentElement.tagName === "TBODY") {
                    let rowLine = "|";
                    const cells = row.getElementsByTagName("td");
                    for (let i = 0; i < cells.length - 1; i++) {
                        const cell = cells[i];
                        const input = cell.querySelector("input");
                        const select = cell.querySelector("select");
                        let value = "";
                        if (input) value = input.value;
                        else if (select) value = select.options[select.selectedIndex].text;
                        rowLine += ` ${value.padEnd(15)} |`;
                    }
                    tableText += rowLine + "n";
                }
            }

            const subject = encodeURIComponent(`${park} Eğitim Takvimi - ${haftaSecimi}`);
            const body = encodeURIComponent(tableText);
            window.location.href = `mailto:gurkan.avci@ibb.gov.tr?subject=${subject}&body=${body}`;
        }

        // Sayfa Yüklendiğinde
        window.onload = function() {
            haftaGuncelle('Topkapi');
            haftaGuncelle('Bagcilar');
            haftaGuncelle('Sancaktepe');
            veriYukle('Topkapi');
            veriYukle('Bagcilar');
            veriYukle('Sancaktepe');
            saatSirala('Topkapi');
            saatSirala('Bagcilar');
            saatSirala('Sancaktepe');
            toplamGuncelle('Topkapi');
            toplamGuncelle('Bagcilar');
            toplamGuncelle('Sancaktepe');
        };
    </script>
</body>
</html>
