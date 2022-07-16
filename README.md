# Proje 1

Bu projede bir öğrenci not sistemi oluşturacaksınız. Sizden istenilenler:
-    Kendinize bir ders belirleyiniz. (Matematik,Fizik, Lineer Cebir vb.)
-   Not aralığınızı oluşturunuz (100-80 ⇒ A, 79-70 ⇒ B vb.)
-   Öğrenci Bilgilerini (Ad, Soyad, Okul No, sınav puanı) girebileceğiniz ve bu bilgilerin tutulabileceği bir sistem oluşturunuz.
-   Girilen bilgilerden yola çıkarak öğrencinin dersi geçip geçmediğini göstermesi gerekmektedir.
-   Öğrenci dersi geçti ise öğrencinin bilgilerinin tutulduğu alana “Geçti” yazısı, öğrenci dersi geçemedi ise “kaldı” yazısını göstermesi gerekmektedir.
-   Notları girilen öğrencilerden dersi geçenleri ve geçmeyenleri gösteren bir Dataframe oluşturunuz.
-   Oluşturulan Dataframe’i Excel tablosuna dönüştürünüz.

# Kod Örnekleri

    ders="Matematik"
    
    print("Matematik dersinde geçip kalan öğrenci tablosu")
    
    ogrenci_adi= "Ali Can"
    
    OgrenciNumarasi=2101
    
    Notlar=[40,50]
    
    ortalama=(float(Notlar[0])*0.4)+(float(Notlar[1])*0.6)#ortalama hesaplama
    
    print("Ortalama :{0}".format(ortalama))
    
      
    
    if(ortalama<=100  and  ortalama>=85):
    
    print("Harf Notu: A (GECT)")
    
    elif(ortalama<=84  and  ortalama>=75):
    
    print("Harf Notu: B (GECTİ)")
    
    elif(ortalama<=74  and  ortalama>=65):
    
    print("Harf Notu: C (GECTİ)")
    
    elif(ortalama<=64  and  ortalama>=55):
    
    print("Harf Notu: D (GECTİ)")
    
    elif(ortalama<=54  and  ortalama>=45):
    
    print("Harf Notu: E (GECTİ)")
    
    elif(ortalama<=44):
    
    print("Harf Notu: F (KALDI!)")
    
    else:
    
    print("Lutfen Gecerli Bir Deger Giriniz!!!!!")
Matematik dersinde geçip kalan öğrenci tablosu

Ortalama :46.0 

Harf Notu: E (GECTİ)


    list = [["Ali Can",2101,46,"Gecti"],["Ayşe Demir",2102,76,"Gecti"],["Fatih Basuk",2100,36,"Kaldı"],["Fatma Tan",2105,50,"Gecti"]]
    
    dict = {"Name":["Ali Can","Ayşe Demir","Fatih Basuk","Fatma Tan"], "Grade": [46,76,36,50]}
    
    dict_list = [
    
    {"Adi": "Ali Can","OgrencıNumarasi":2101, "Ortalama":46, "Sonuc":"Gecti"},
    
    {"Adi": "Ayşe Demir","OgrencıNumarasi":2102, "Ortalama":76, "Sonuc":"Gecti"},
    
    {"Adi": "Fatih Basuk","OgrencıNumarasi":2100, "Ortalama":36, "Sonuc":"Kaldi"},
    
    {"Adi": "Fatma Tan","OgrencıNumarasi":2105, "Ortalama":50, "Sonuc":"Gecti"}
    
    ]
    
    df = pd.DataFrame(dict_list, index = [0,1,2,3])
    
    def  session_control():
    
    dosya_listesi = os.listdir()
    
    if  "Notlar.xlsx"in  dosya_listesi:
    
    return  True
    
      
    
    else:
    
    return  False
    
    if  session_control()==False:
    
    df.to_excel("Notlar.xlsx")
    
    print(df)


![enter image description here](https://github.com/tubabalkan/GlobalAIHub-Homework/blob/main/ckt1.png)
## Excel Çıktısı
![enter image description here](https://github.com/tubabalkan/GlobalAIHub-Homework/blob/main/%C3%96rnek-%C3%87%C4%B1kt%C4%B1.png)


