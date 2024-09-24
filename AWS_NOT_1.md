# 🌐 AWS Certified Solutions Architect – Associate

---

## 📋 1. Sınavın Temelleri ve Formatı

- **Soru Sayısı**: 65 soru
- **Soru Türleri**: 
  - **Çoktan Seçmeli** (Tek doğru cevap)
  - **Çoklu Yanıt** (Birden fazla doğru cevap)
- **Sınav Süresi**: 130 dakika
- **Geçme Notu**: %70-75 civarı
- **Sınav Ücreti**: 150 USD
- **Deneme Sınavı Ücreti**: 20 USD (isteğe bağlı)

### 🎯 Sınavda Kapsanan Konular ve Ağırlıkları

| Konu                                         | Ağırlık (%) |
|----------------------------------------------|-------------|
| 🔒 Design Secure Architectures                | 30          |
| 🔄 Design Resilient Architectures            | 26          |
| ⚡ Design High-Performing Architectures      | 24          |
| 💰 Design Cost-Optimized Architectures       | 20          |

### 📅 Tavsiye Edilen Hazırlık Süreci

- **6-8 hafta**: Planlı çalışmak için ideal süre.
- **Günlük Çalışma**: Her gün düzenli olarak konu tekrarı ve pratik yapın.
- **Deneme Sınavları**: Haftada bir deneme sınavı çözerek performansınızı ölçün.

---

## 🔒 2. Design Secure Architectures (Güvenli Mimariler Tasarlama) - %30

### A. **Güvenlik Temelleri**

#### 1. **IAM (Identity and Access Management)**
- **Kullanıcı ve Grup Politikaları**: IAM kullanarak yetkilendirme ayarlarını yapılandırın.
- **IAM Role**: Servislerin birbirleriyle güvenli etkileşim kurmasını sağlar.
- **IAM Policies**: JSON formatında kaynaklara erişim haklarını belirleyin.
- **IAM Conditions**: Erişimi zaman, IP adresi gibi faktörlere göre kısıtlayın.
- **MFA (Multi-Factor Authentication)**: Çift faktörlü kimlik doğrulama uygulayın.

#### 2. **KMS (Key Management Service)**
- **Şifreleme Anahtarları Yönetimi**: Verilerinizi şifrelemek için KMS kullanın.
- **Customer Master Keys (CMK)**: Kullanıcı tanımlı anahtarlar ile verilerinizi koruyun.
- **Envelope Encryption**: Veri ve anahtarları şifreleyin.

#### 3. **S3 Bucket Policies ve ACLs**
- **Erişim Kontrolü**: Public/Private erişimi yönetin.
- **S3 Versioning**: Eski sürümleri saklayarak geri dönebilme yeteneği.

#### 4. **AWS Shield & WAF**
- **AWS Shield**: DDoS saldırılarına karşı koruma.
- **WAF**: Web uygulamalarını güvenlik açıklarına karşı koruyun.

#### 5. **Security Groups ve Network ACLs**
- **Security Groups**: Instance seviyesinde gelen ve giden trafiği kontrol edin.
- **Network ACLs**: Alt ağ seviyesinde kuralları belirleyin.

#### 6. **CloudTrail**
- **Aktivite İzleme**: AWS hesap aktivitelerini ve API çağrılarını kaydedin.

#### 7. **VPC Peering**
- **Güvenli Bağlantılar**: Farklı VPC’ler arasında özel bağlantılar oluşturun.

---

## 🔄 3. Design Resilient Architectures (Dayanıklı Mimariler Tasarlama) - %26

### A. **Yüksek Erişilebilirlik (High Availability)**

#### 1. **EC2 Auto Scaling**
- **Otomatik Ölçeklendirme**: Talebe göre yeni instance başlatır veya kaynakları azaltır.
- **Launch Configurations ve Auto Scaling Groups**: Kaynak optimizasyonunu yönetin.

#### 2. **Multi-AZ Deployments**
- **Yüksek Dayanıklılık**: EC2, RDS gibi hizmetleri birden fazla Availability Zone’a dağıtarak güvenliği artırın.

#### 3. **Elastic Load Balancer (ELB)**
- **ALB**: HTTP/HTTPS için gelişmiş yönlendirme.
- **NLB**: Düşük gecikme süreli TCP trafiği.
- **Cross-Zone Load Balancing**: Farklı AZ’ler arasında yük dengelemesi yapın.

### B. **Felaket Kurtarma (Disaster Recovery)**

#### 1. **Backup and Restore**
- **Yedekleme**: Verilerinizi Amazon S3 veya Amazon Glacier ile yedekleyin.

#### 2. **Pilot Light**
- **Kritik Bileşenler**: Önemli bileşenlerin çalışır durumda tutulması.

#### 3. **Warm Standby**
- **Hızlı Genişletme**: Düşük kapasitede çalışan sistemler gerektiğinde hızla artırılabilir.

#### 4. **Multi-Site**
- **Aktif Yedeklilik**: İki site arasında yük paylaşımı yaparak kesintileri minimize edin.

### C. **Yedeklilik ve İyileşme**

#### 1. **Route 53**
- **DNS Failover**: Kesinti durumunda yedek sunucuya geçiş.

#### 2. **RDS Multi-AZ ve Read Replicas**
- **Multi-AZ**: Yüksek kullanılabilirlik ve otomatik yedeklilik.
- **Read Replicas**: Okuma yükünü dengelemek için kullanın.

---

## ⚡ 4. Design High-Performing Architectures (Yüksek Performanslı Mimariler Tasarlama) - %24

### A. **Compute Performansı**

#### 1. **EC2 Instance Türleri**
- **T Serisi**: Küçük ve aralıklı iş yükleri için.
- **M Serisi**: Genel amaçlı kullanım.
- **C Serisi**: Hesaplama yoğun iş yükleri için.
- **R Serisi**: Bellek yoğun iş yükleri için.
- **Spot Instances**: Maliyet avantajı sağlar.

#### 2. **Lambda**
- **Sunucusuz Fonksiyonlar**: Yalnızca kullanıldıklarında ücret ödeyin.
- **Lambda Layers**: Paylaşımlı kod ve bağımlılıkları yönetin.

### B. **Veri Depolama Performansı**

#### 1. **Amazon S3**
- **Transfer Acceleration**: Hızlı veri aktarımı.
- **Lifecycle Policies**: Veri depolama sınıflarını otomatik geçiş kurallarıyla yönetin.

#### 2. **Amazon EFS (Elastic File System)**
- **Paylaşımlı Dosya Sistemi**: EC2 instance'lar arasında otomatik ölçeklenebilir.

#### 3. **Amazon Glacier**
- **Uzun Süreli Arşivleme**: Düşük maliyetli veri arşivleme çözümü.

### C. **Veritabanı Performansı**

#### 1. **Amazon RDS**
- **Otomatik Yedekleme**: Veritabanı performansı ve yüksek kullanılabilirlik.

#### 2. **DynamoDB**
- **NoSQL Çözümü**: Yüksek performans ve düşük gecikme süreleri.
- **DAX (DynamoDB Accelerator)**: Sorguları hızlandırır.

#### 3. **Amazon Redshift**
- **Büyük Veri Analitiği**: Veri ambarı ve sorgu hızlandırma çözümü.

---

## 💰 5. Design Cost-Optimized Architectures (Maliyet-Optimize Mimariler Tasarlama) - %20

### A. **Maliyet Yönetimi**

#### 1. **AWS Budgets**
- **Harcama Bütçeleri**: Harcama limitleri belirleyin ve uyarılar oluşturun.

#### 2. **Cost Explorer**
- **Harcama Analizleri**: Maliyet optimizasyonu için analiz yapın.

#### 3. **Cost Allocation Tags**
- **Kaynak Etiketleme**: Detaylı maliyet yönetimi için kaynakları etiketleyin.

### B. **EC2 Maliyet Optimizasyonu**

#### 1. **Right-Sizing**
- **Instance Boyutlandırma**: İhtiyacınıza uygun boyutları seçin.

#### 2. **Reserved Instances**
- **Taahhüt ile Düşük Maliyet**: Uzun vadeli kullanım için avantaj sağlayın.

#### 3. **Spot Instances**
- **Maliyet Avantajı**: Düşük öncelikli işler için kullanın.

### C. **Depolama Maliyet Optimizasyonu**

#### 1. **S3 Lifecycle Policies**
- **Otomatik Geçiş**: Verilerinizi uygun maliyetli depolama sınıflarına taşıyın.

#### 2. **Data Transfer Costs**
- **Ücretsiz VPC İçi Veri Transferleri**: Dışa veri transferi maliyetlerini optimize edin.

---

## 📘 Ekstra Bilgiler

### A. **Well-Architected Framework**
- AWS’in rehberlerini inceleyerek en iyi uygulamalar geliştirin.

### B. **AWS Whitepapers**
- AWS’in sağladığı dökümanları okuyarak konular hakkında derin bilgi edinin.

---

## 🧠 Hazırlık Tavsiyeleri
1. **Deneme Sınavları**: Sınav formatına alışmak için deneme sınavları çözün.
2. **Pratik Yapın**: AWS hizmetlerini pratik projelerde uygulayarak teorik bilgileri pekiştirin.
3. **Whitepapers**: AWS’in önerdiği whitepaper’ları okuyarak bilgi derinliğinizi artırın.
