# Azure DevOps CI/CD ile Kubernetes Deployment Projesi

Bu proje, modern DevOps süreçlerini simüle etmek amacıyla; **Azure DevOps Pipelines**, **Self-Hosted Agent** ve **Kubernetes (Docker Desktop/Local)** kullanılarak uçtan uca bir CI/CD hattının kurulmasını kapsamaktadır.

Proje, .NET Core tabanlı örnek bir web uygulamasının otomatik olarak derlenmesini (Build) ve yerel Kubernetes ortamına kesintisiz bir şekilde dağıtılmasını (Deploy) sağlar.

## 🚀 Proje Amacı

* **Otomasyon:** Kod  değişikliklerinin (Push) otomatik olarak algılanıp sürecin başlatılması.
* **Konteynerizasyon:** Uygulamanın Docker ile paketlenip imaj haline getirilmesi.
* **Orkestrasyon:** Kubernetes deployment ve servis objeleri ile uygulamanın  yönetilmesi.
* **Altyapı:** Kendi bilgisayarımızda çalışan (Self-hosted) bir Azure Agent ile bulut ve yerel ortamın konuşturulması.

## 📂 Repo Yapısı

aşağıdaki dosya yapısına sahiptir  :

```text
.
├── deployment.yaml       # Kubernetes Deployment konfigürasyonu (Replica, Limits, Probes)
├── service.yaml          # Uygulamaya erişim için LoadBalancer servis tanımı
├── Dockerfile            # Uygulamanın Docker imajını oluşturma talimatları
├── azure-pipelines.yaml  # CI/CD sürecini yöneten pipeline dosyası
├── aspnetapp             # Uygulama kaynak kodları
└── README.md             # Proje dokümantasyonu