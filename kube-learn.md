# Things to know before learning kubernetes

## Monolith to Microservices

Monolith: semua service di develop di dalam satu aplikasi 
Microservices: kebalikannya, dipecah jadi kecil-kecil, tiap aplikasi megurus satu tugas dengan baik dan semua aplikasi saling berkomunikasi

Problem: kalau mau di scale gimana?
Solution: Pindah dari VM ke Container

## Virtual Machine vs Container
Virtual Machine: Butuh waktu, makan resource, lamban, bikin mesin di atas mesin (harus virtualisasi komponen dari ram, disk, cpu dll.)
Container: Pakai Container Manager, Aplikasi running di dalam satu container, OSnya menggunakan OS bawaan hostnya (VMnya)

- Pakai VM harus nungu boot process dulu, container langsung jalan lebih cepet
- Container: Docker, Podman, Conteinerd

Docker Deployment:
1. Dev minta buatin image dan oush ke container registry
2. Docker buat image (build) pakai Dockerfile
3. Docker kirim image (push) aplikasi yang sudah jadi ke container registry
4. Dev minta docker di production buat jalanin image ke production infra
5. Docker ambil image dari container registry
6. Docker running container pake image yang sudah di pull

Sebelum Lanjut pastikan belajar docker/container terlebih dahulu


# Intro to Kubernetes

## What is Kubernetes?
Aplikasi buat automation deployment, scaling, dan manajemen aplikasi berbasis container. Intinya buat ngatur container lah bisar bisa macem-macem.


## History of Kubernetes
Awalnya dari google yang namanya borg, terus jadi omega, terus jadi kubernetes, dibuat pake bahasa pemrograman golang.


## Kubernetes Workflow
1. DevOps, Infra bikin manifest/configuration file yang isinya tentang spesifikasi containernya sesuai dengan kebutuhan
2. Misal config dibuat dengan spesifikasi, CPU sekian, Memory sekian, image sekian, dan kebutuhan lainnya.
3. Apply manifest/config ke master node kubernetes, Dari master bakal nturuh worker buat jalanin aplikasinya.



