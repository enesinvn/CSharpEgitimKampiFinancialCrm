💰 Financial CRM - Finansal Müşteri İlişkileri Yönetim Sistemi

**C# Windows Forms** ve **Entity Framework** ile geliştirilmiş profesyonel bir finansal yönetim uygulaması.

## 🚀 Proje Özellikleri

### 🔐 Güvenlik
- **Login Sistemi** - Entity Framework ile kullanıcı doğrulama
- **Session Management** - Güvenli form geçişleri
- **Kullanıcı Yönetimi** - CRUD işlemleri ile kullanıcı yönetimi

### 🏦 Banka Yönetimi
- **Banka Hesapları** - Tam CRUD işlemleri
- **Banka İşlemleri** - Giriş/Çıkış işlem takibi
- **Bakiye Yönetimi** - Otomatik bakiye hesaplama
- **İşlem Geçmişi** - Detaylı işlem kayıtları

### 💳 Harcama Takibi
- **Harcama Kategorileri** - Kategori bazlı organizasyon
- **Harcama Kayıtları** - Tarih, tutar ve kategori ile kayıt
- **Filtreleme** - Kategoriye göre filtreleme
- **Raporlama** - Günlük/aylık harcama raporları

### 💰 Fatura Yönetimi
- **Fatura Ekleme/Düzenleme** - Tam CRUD işlemleri
- **Dönemsel Takip** - Fatura dönemlerinin yönetimi
- **Tutar Hesaplama** - Otomatik toplam hesaplama

### 📊 Dashboard & Raporlama
- **Grafik Görselleştirme** - Chart kontrolü ile verinin görselleştirilmesi
- **Gerçek Zamanlı İstatistikler** - Canlı veri takibi
- **Mali Durum Özeti** - Toplam bakiye, harcama ve gelir özeti
- **Fatura Bilgilendirme** - Otomatik döngüsel fatura gösterimi

## 🛠️ Teknolojiler

### Backend
- **C# .NET Framework 4.7.2**
- **Entity Framework 6** (Database First)
- **LINQ** - Veri sorguları
- **SQL Server** - Veritabanı

### Frontend
- **Windows Forms** - Desktop UI
- **Chart Controls** - Grafik görselleştirme
- **Modern UI Design** - Renkli ve kullanıcı dostu arayüz

### Mimari
- **3-Tier Architecture** - UI, Business Logic, Data Access
- **Repository Pattern** - Veri erişim katmanı
- **Entity Framework Code First** yaklaşımı

## 📋 Veritabanı Şeması

```sql
-- Kullanıcılar
Users: UserId, Username, Password

-- Banka Bilgileri
Banks: BankId, BankTitle, BankAccountNumber, BankBalance

-- Banka İşlemleri
BankProcesses: BankProcessId, Description, ProcessDate, ProcessType, Amount, BankId

-- Kategoriler
Categories: CategoryId, CategoryName

-- Harcamalar
Spendings: SpendingId, SpendingTitle, SpendingAmount, SpendingDate, CategoryId

-- Faturalar
Bills: BillId, BillTitle, BillAmount, BillPeriod
```

## 🎯 Kullanım

### 1. Giriş
- Uygulamayı başlatın
- Kullanıcı adı ve şifrenizi girin 
- Ana menüye erişim sağlayın

### 2. Navigation
- **Dashboard**: Genel mali durum ve grafikler
- **Bankalar**: Banka hesapları yönetimi
- **Banka İşlemleri**: Gelir/gider işlemleri
- **Kategoriler**: Harcama kategorileri
- **Harcamalar**: Harcama kayıtları
- **Faturalar**: Fatura yönetimi

### 3. Temel İşlemler
```csharp
// Örnek: Yeni harcama ekleme
var spending = new Spendings()
{
    SpendingTitle = "Market Alışverişi",
    SpendingAmount = 150.00m,
    SpendingDate = DateTime.Now,
    CategoryId = 1
};
db.Spendings.Add(spending);
db.SaveChanges();
```

## 📸 Ekran Görüntüleri
<img width="438" height="402" alt="Ekran görüntüsü 2025-08-30 003557" src="https://github.com/user-attachments/assets/9eae9263-eb40-42d2-bac9-54f028d677ca" />
<img width="686" height="518" alt="Ekran görüntüsü 2025-08-30 003719" src="https://github.com/user-attachments/assets/d88f2040-fc3d-48f3-b309-062a9dc1312c" />
<img width="986" height="566" alt="Ekran görüntüsü 2025-08-30 003752" src="https://github.com/user-attachments/assets/0bbcf64d-d464-4b12-a046-a74c29e31a78" />
<img width="988" height="569" alt="Ekran görüntüsü 2025-08-30 003806" src="https://github.com/user-attachments/assets/6c767623-2329-4c92-a047-6aa932b35714" />
<img width="1184" height="622" alt="Ekran görüntüsü 2025-08-30 004134" src="https://github.com/user-attachments/assets/2b62aea7-9c50-40d2-97dc-63a57152af1b" />
<img width="684" height="519" alt="Ekran görüntüsü 2025-08-30 003828" src="https://github.com/user-attachments/assets/ec124da1-8a23-45ea-bb8e-33f3438d2439" />

### Dashboard
- 📊 Banka bakiyesi grafikleri
- 💰 Toplam mali durum
- 📈 Aylık harcama trendleri

### CRUD İşlemleri
- ✅ **Create**: Yeni kayıt ekleme
- ✅ **Read**: Kayıtları listeleme ve filtreleme
- ✅ **Update**: Kayıt güncelleme
- ✅ **Delete**: Güvenli kayıt silme

## 🔄 Proje Mimarisi

```
FinancialCrm/
├── Models/              # Entity Framework Modelleri
│   ├── Banks.cs
│   ├── BankProcesses.cs
│   ├── Categories.cs
│   ├── Spendings.cs
│   ├── Bills.cs
│   └── Users.cs
├── Forms/               # Windows Forms
│   ├── FrmLogin.cs
│   ├── FrmMainMenu.cs
│   ├── FrmDashboard.cs
│   ├── FrmBanks.cs
│   ├── FrmBankProcesses.cs
│   ├── FrmCategories.cs
│   ├── FrmSpendings.cs
│   └── FrmBilling.cs
├── App.config          # Veritabanı bağlantı ayarları
└── Program.cs          # Uygulama giriş noktası
```

## 🚀 Özellikler

### ✅ Tamamlanan
- [x] Login sistemi ve kullanıcı doğrulama
- [x] Tam CRUD işlemleri (tüm tablolar için)
- [x] Entity Framework entegrasyonu
- [x] Modern UI tasarımı
- [x] Grafik görselleştirme
- [x] Validation kontrolleri
- [x] İlişkisel veri yönetimi
- [x] Session management
- [x] Otomatik hesaplamalar

### 🔄 Geliştirilebilecek
- [ ] Raporlama modülü (PDF export)
- [ ] Email bildirimleri
- [ ] Multi-language support
- [ ] API entegrasyonu
- [ ] Mobile responsive design


## 👤 Geliştirici

**Enes İnan**
- GitHub: [@enesinvn](https://github.com/enesinvn)
- Email: [e.invn17@gmail.com](e.invn17@gmail.com)

## 🙏 Teşekkürler

Bu proje Murat Yücedağ hacamın **C# Eğitim Kampı** kapsamında geliştirilmiştir. Kendisine bu eğitim süreci için en içten dileklerimi sunuyorum çok faydalı bir eğitim oldu. Her şey için teşekkürler.

---

⭐ **Bu projeyi faydalı bulduysanız yıldız vermeyi unutmayın!**

## 🏷️ Tags

`csharp` `winforms` `entity-framework` `sql-server` `financial` `crm` `desktop-app` `dotnet` `linq` `database-first`
