# Yazılım 101 Bitirme Projesi

Bu projede kurs sürecinde işlenen bütün konuları içermesi amaçlanmıştır. 

# Proje açıklaması
Bir hastane randevu uygulaması yazınız. Bu uygulama, API üzerinden aldığı komutları işleyerek, gerekli işlemleri yapması gerekmektedir. Uygulama kullanıcıya 3 farklı api sunmalı.
 
 # API Açıklaması
 1 . Doktor API ("v1/doctor")
 ---
    
   Doktor api (DoctorAPI) üzerinden kullanıcı tüm doktorları listeleme, doktor id ile doktor görüntüleme doktor ekleme, silme ve güncelleme işlemleri (CRUD) yapabilmelidir (CRUD). Doktor modellemesi aşağıda ayrıca açıklanmıştır.
  
  
  2 . Hasta API ("v1/patient")
 ---
   
   Hasta api (PatientAPI) üzerinden kullanıcı, hasta ekleme, silme, güncelleme ve tüm hastaları listeleme, hasta id ile hasta görüntüleme işlemleri yapabilmelidir. (CRUD). Hasta modellemesi aşağıda ayrıca açıklanmıştır.
   
   
   3 . Randevu API ("v1/appointment")
 ---
   
   Randevu api (AppointmentAPI) üzerinden kullanıcı yeni randevu oluşturma, randevu görüntüleme, tüm randevuları listeleme, güncelleme ve randevu silme işlemleri yapabilmelidir (CRUD). Hasta modellemesi aşağıda ayrıca açıklanmıştır.
   
# Modeller
  
  ## Doctor
  
  - id (tckn) (String)
  - name (String)
  - namePrefix (Dr., Prof., Doc., Uzm., vb) (Enum type)
  - department (Enum type)
  - dateOfGraduate (yıl) (Integer)
  - dateOfStart (yıl) (Integer)
  
  ## Patient
  
  - id (tckn) (String)
  - name (String)
  - gender (Enum type)
  - dateOfBirth (yıl) (Integer)
  - city (Enum type)
  - address (String)
  - healthInsurance (boolean)
  
  ## Appointment

  - id (auto increment) (Integer)
  - docktorId (String)
  - patientId (String)
  - date (String)
  - hour (Integer)
  - minute (Integer)
  - notes (String)
 
# Mimari

  - Proje bir SpringBoot projesi olmalı. İçerisinde Spring Web, Spring JPA kütüphaneleri eklenmeli. Lombok kütüphanesi kullanılabilir ancak zorunlu değildir.
  
  - DoctorAPI, PatienceAPI, AppointmentAPI birer RestController olmalıdır. Alınan istekler ilgili servis katmanına iletilerek veri tabanı kaydı yapılmalıdır. RestController'lar Dto (Data Transfer Object) dönmelidir. 
  
  - Veri tabanı olarak H2 Veritabanı kullanılmalıdır.
  
  - Modeller arasında mantıksal ilişki kurulmasına gerek yok. Derste işlediğimiz gibi, gerekiyorsa sorgulama yaparak ilgili kaydın olup olmadı kontrol edilebilir. 
  
  - Bir servis sadece ilişkili repository katmanına ulaşmalı. Farklı bir model sorgulaması yapmaya ihtiyaç duyulursa ilgili servis üzerinden sorgulanmalı.
  
  - Değişken, fonksiyon ve sınıf isimleri Ingilizce olmalıdır. 
  
  
  
   
   

    
    
    
