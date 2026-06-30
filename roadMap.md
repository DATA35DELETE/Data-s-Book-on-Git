# Data's Book on Git
 
## Git
 
### Ön Söz
- Ben kimim?
- Bu Data's Book on Git nedir?
- Bu dokümantasyon ne öğretecek?
 
---
 
### Git : Giriş
- **Versiyon Kontrol Sistemi Nedir?**: Tanım. Neden Gerekli? Kullanım Senaryoları.
  - **VCS Olmadan Çalışmak**: Sorunlar. Dosya Karmaşası. Örnek.
  - **VCS Türleri**: Local. Centralized. Distributed. Tablo Halinde.
- **Git Nedir?**: Tanım. Kısa Tarihçesi. Linus Torvalds.
  - **Git vs SVN vs Mercurial**: Karşılaştırma. Tablo Halinde.
  - **Dağıtık Yapı**: Herkesin Tam Kopyası. Avantajları.
- **Git Kurulumu**:
  - **Linux**: `apt install git`. Örnek.
  - **macOS**: Homebrew ile. `brew install git`. Örnek.
  - **Windows**: Git for Windows. Git Bash. Örnek.
  - **Versiyon Kontrolü**: `git --version`. Örnek.
- **İlk Yapılandırma**:
  - **Kullanıcı Adı**: `git config --global user.name`. Örnek.
  - **E-posta**: `git config --global user.email`. Örnek.
  - **Varsayılan Editor**: `git config --global core.editor`. VS Code. Vim. Örnek.
  - **Varsayılan Branch Adı**: `git config --global init.defaultBranch main`. Örnek.
  - **Config Görüntüleme**: `git config --list`. Örnek.
  - **Config Seviyeleri**: `--local`. `--global`. `--system`. Farkları. Tablo Halinde.
- **Git'in Çalışma Mantığı**: Snapshot Tabanlı Yapı. Delta ile Farkı. Örnek.
  - **Üç Bölge**: Working Directory. Staging Area. Repository. Görselleştirme.
  - **Dosya Durumları**: Untracked. Tracked. Modified. Staged. Committed. Tablo Halinde.
- **Yardım Alma**: `git help`. `git <komut> --help`. Örnek.
 
---
 
### Git : Temel İş Akışı
- **Repository (Repo) Nedir?**: Tanım. `.git` Klasörü. Örnek.
- **git init**: Tanım. Yeni Repo Oluşturma. Örnek.
  - **Mevcut Projeyi Git'e Alma**: Adım Adım. Örnek.
- **git status**: Tanım. Dosya Durumlarını Görme. Örnek.
  - **Short Format**: `git status -s`. Örnek.
- **git add**: Tanım. Dosyaları Sahneye Alma.
  - **Tek Dosya**: `git add dosya.txt`. Örnek.
  - **Tüm Dosyalar**: `git add .`. Örnek.
  - **Belirli Uzantı**: `git add *.c`. Örnek.
  - **İnteraktif**: `git add -i`. Örnek.
- **git commit**: Tanım. Değişiklikleri Kaydetme.
  - **Temel Kullanım**: `git commit -m "mesaj"`. Örnek.
  - **Editor ile Commit**: `git commit`. Uzun Mesaj. Örnek.
  - **İyi Commit Mesajı Yazmak**: Kural ve Prensipler. Örnek.
  - **Conventional Commits**: Tanım. `feat:`. `fix:`. `docs:`. Tablo Halinde.
- **git log**: Tanım. Commit Geçmişini Görme.
  - **Temel Kullanım**: Örnek.
  - **`--oneline`**: Kısa Format. Örnek.
  - **`--graph`**: Dal Grafiği. Örnek.
  - **`-p`**: Değişiklikleri Göster. Örnek.
  - **`--stat`**: Dosya İstatistikleri. Örnek.
- **git diff**: Tanım. Değişiklikleri Karşılaştırma.
- **git show**: Tanım. Commit Detayını Görme. Örnek.
 
---
 
### Git : .gitignore
- **.gitignore Nedir?**: Tanım. Neden Kullanılır? Kullanım Senaryoları.
- **Temel Sözdizimi**: Kalıplar. Wildcards. Negasyon. Örnek.
  - **Dosya Yoksayma**: `dosya.txt`. Örnek.
  - **Klasör Yoksayma**: `klasor/`. Örnek.
  - **Uzantı Yoksayma**: `*.log`. Örnek.
  - **Negasyon**: `!önemli.log`. Örnek.
  - **Yorum Satırı**: `#`. Örnek.
- **Yaygın .gitignore Şablonları**: C/C++. Python. Node.js. Java. Tablo Halinde.
- **Zaten Takip Edilen Dosyaları Yoksaymak**: `git rm --cached`. Örnek.
- **Global .gitignore**: `~/.gitignore_global`. Tanım. Kurulum. Örnek.
- **gitignore.io**: Tanım. Otomatik Şablon Üretme. Örnek.
 
---
 
### Git : Branch (Dal) Yönetimi
- **Branch Nedir?**: Tanım. Neden Kullanılır? Görselleştirme.
  - **HEAD Nedir?**: Tanım. Aktif Branch Göstergesi. Örnek.
  - **main / master**: Varsayılan Branch. Tanım.
- **git branch**: Tanım. Branch Listeleme.
  - **Branch Listeleme**: `git branch`. Örnek.
  - **Tüm Branch'ler**: `git branch -a`. Örnek.
  - **Branch Oluşturma**: `git branch isim`. Örnek.
  - **Branch Silme**: `git branch -d isim`. Örnek.
  - **Zorla Silme**: `git branch -D isim`. Örnek.
  - **Branch Yeniden Adlandırma**: `git branch -m eski yeni`. Örnek.
- **git switch**: Tanım. Branch Değiştirme. (Modern Yöntem)
  - **Branch'e Geçiş**: `git switch isim`. Örnek.
  - **Oluştur ve Geç**: `git switch -c isim`. Örnek.
- **git checkout**: Tanım. Eski Yöntem. switch ile Farkı.
  - **Branch'e Geçiş**: `git checkout isim`. Örnek.
  - **Oluştur ve Geç**: `git checkout -b isim`. Örnek.
  - **Dosyayı Geri Al**: `git checkout -- dosya`. Örnek.
- **Branch Stratejileri**: Tanım. Kullanım Senaryoları.
  - **Feature Branch**: Tanım. Örnek.
  - **Git Flow**: Tanım. main. develop. feature. release. hotfix. Örnek.
  - **GitHub Flow**: Tanım. Basit Yapı. Örnek.
  - **Trunk Based Development**: Tanım. Örnek.
 
---
 
### Git : Merge (Birleştirme)
- **Merge Nedir?**: Tanım. Branch'leri Birleştirme. Görselleştirme.
- **git merge**: Tanım. Sözdizimi. Örnek.
  - **Fast-Forward Merge**: Tanım. Ne Zaman Olur? Görselleştirme. Örnek.
  - **3-Way Merge**: Tanım. Merge Commit. Görselleştirme. Örnek.
  - **`--no-ff`**: Fast-Forward'ı Engelleme. Neden Kullanılır? Örnek.
  - **`--squash`**: Tanım. Commit'leri Tek'e İndirme. Örnek.
- **Merge Çakışması (Conflict)**: Tanım. Neden Olur? Örnek.
  - **Çakışma İşaretleri**: `<<<<<<<`, `=======`, `>>>>>>>`. Tanım.
  - **Manuel Çözüm**: Adım Adım. Örnek.
  - **`git mergetool`**: Tanım. Araç Seçimi. Örnek.
  - **Merge'i İptal Etmek**: `git merge --abort`. Örnek.
- **Merge Sonrası Temizlik**: Branch Silme. Örnek.
 
---
 
### Git : Rebase
- **Rebase Nedir?**: Tanım. Merge ile Farkı. Görselleştirme.
  - **Ne Zaman Kullanılır?**: Kullanım Senaryoları.
  - **Altın Kural**: Public Branch'lerde Rebase Yapma. Neden?
- **git rebase**: Tanım. Sözdizimi. Örnek.
  - **Temel Rebase**: `git rebase main`. Örnek.
  - **Çakışma Yönetimi**: `git rebase --continue`. `git rebase --abort`. Örnek.
- **Interactive Rebase**: Tanım. `git rebase -i`. Kullanım Senaryoları.
  - **pick**: Commit'i Koru. Örnek.
  - **reword**: Commit Mesajını Değiştir. Örnek.
  - **edit**: Commit'i Düzenle. Örnek.
  - **squash**: Önceki Commit ile Birleştir. Örnek.
  - **fixup**: squash ama Mesajı At. Örnek.
  - **drop**: Commit'i Sil. Örnek.
  - **reorder**: Commit Sırası Değiştirme. Örnek.
- **Rebase vs Merge**: Tablo Halinde Karşılaştırma. Hangi Durumda Ne?
 
---
 
### Git : Geçmişi Düzenleme
- **Son Commit'i Değiştirme**: `git commit --amend`. Tanım. Örnek.
  - **Sadece Mesajı Değiştirme**: Örnek.
  - **Dosya Ekleme/Çıkarma**: Örnek.
- **git reset**: Tanım. Commit'leri Geri Alma.
  - **`--soft`**: Commit'i Geri Al. Değişiklikler Staged'de. Örnek.
  - **`--mixed`** *(varsayılan)*: Commit'i Geri Al. Değişiklikler Working Directory'de. Örnek.
  - **`--hard`**: Commit'i ve Değişiklikleri Tamamen Sil. Dikkat! Örnek.
- **git revert**: Tanım. Güvenli Geri Alma. reset ile Farkı. Örnek.
  - **Ne Zaman revert Ne Zaman reset?**: Tablo Halinde.
- **git restore**: Tanım. Dosyaları Geri Yükleme. (Modern Yöntem)
  - **Working Directory'yi Geri Al**: `git restore dosya`. Örnek.
  - **Staging'den Geri Al**: `git restore --staged dosya`. Örnek.
- **git clean**: Tanım. Takip Edilmeyen Dosyaları Silme.
  - **`-n`**: Önizleme. Dry Run. Örnek.
  - **`-f`**: Zorla Sil. Örnek.
  - **`-fd`**: Klasörleri de Sil. Örnek.
 
---
 
### Git : Stash
- **git stash Nedir?**: Tanım. Kullanım Senaryoları. Örnek.
- **Temel Kullanım**:
  - **Stash'e Al**: `git stash`. Örnek.
  - **Mesajla Stash**: `git stash push -m "mesaj"`. Örnek.
  - **Untracked Dosyaları da Al**: `git stash -u`. Örnek.
  - **Listeye Bak**: `git stash list`. Örnek.
  - **Uygula ve Bırak**: `git stash pop`. Örnek.
  - **Sadece Uygula**: `git stash apply stash@{n}`. Örnek.
  - **Belirli Stash'i Sil**: `git stash drop stash@{n}`. Örnek.
  - **Tümünü Sil**: `git stash clear`. Örnek.
- **Stash'ten Branch Oluşturma**: `git stash branch isim`. Tanım. Örnek.
- **Stash İçeriğini Görme**: `git stash show -p`. Örnek.
 
---
 
### Git : Tag (Etiket)
- **Tag Nedir?**: Tanım. Kullanım Senaryoları. Sürüm İşaretleme.
- **Tag Türleri**:
  - **Lightweight Tag**: Tanım. Örnek.
  - **Annotated Tag**: Tanım. Farkı. Örnek.
- **Temel Kullanım**:
  - **Tag Oluşturma**: `git tag v1.0.0`. Örnek.
  - **Annotated Tag**: `git tag -a v1.0.0 -m "mesaj"`. Örnek.
  - **Geçmiş Commit'e Tag**: `git tag v1.0.0 <commit-hash>`. Örnek.
  - **Tag Listeleme**: `git tag`. Örnek.
  - **Tag Detayı**: `git show v1.0.0`. Örnek.
  - **Tag Silme**: `git tag -d v1.0.0`. Örnek.
- **Semantic Versioning**: Tanım. `MAJOR.MINOR.PATCH`. Kurallar. Örnek.
- **Remote'a Tag Gönderme**: `git push origin v1.0.0`. `git push --tags`. Örnek.
- **Remote'dan Tag Silme**: `git push origin --delete v1.0.0`. Örnek.
 
---
 
### Git : Uzak Depo (Remote) İşlemleri
- **Remote Nedir?**: Tanım. Uzak Sunucu. Kullanım Senaryoları.
- **git remote**: Tanım. Remote Yönetimi.
  - **Remote Listeleme**: `git remote -v`. Örnek.
  - **Remote Ekleme**: `git remote add origin <url>`. Örnek.
  - **Remote Silme**: `git remote remove origin`. Örnek.
  - **Remote Yeniden Adlandırma**: `git remote rename`. Örnek.
  - **Remote URL Değiştirme**: `git remote set-url`. Örnek.
- **git clone**: Tanım. Repo Kopyalama.
  - **HTTPS ile Clone**: Örnek.
  - **SSH ile Clone**: Örnek.
  - **Belirli Branch**: `git clone -b branch_adi`. Örnek.
  - **Sığ Kopyalama**: `git clone --depth 1`. Tanım. Örnek.
- **git fetch**: Tanım. Değişiklikleri İndir. merge Yapmaz.
  - **Tüm Remote'ları Fetch**: `git fetch --all`. Örnek.
  - **Remote Branch'leri Görme**: Örnek.
- **git pull**: Tanım. fetch + merge. Örnek.
  - **`--rebase`**: fetch + rebase. Tanım. Örnek.
  - **`--ff-only`**: Sadece Fast-Forward. Örnek.
- **git push**: Tanım. Değişiklikleri Gönderme.
  - **Temel Push**: `git push origin main`. Örnek.
  - **İlk Push**: `git push -u origin main`. Upstream Ayarlama. Örnek.
  - **Tag Push**: Örnek.
  - **Branch Silme**: `git push origin --delete branch`. Örnek.
  - **Zorla Push**: `git push --force`. `--force-with-lease`. Farkı. Dikkat!
- **Upstream Takibi**: Tanım. Remote Tracking Branch. Örnek.
- **Birden Fazla Remote**: Tanım. Kullanım Senaryoları. Örnek.
 
---
 
### Git : SSH ve Kimlik Doğrulama
- **SSH Nedir?**: Tanım. HTTPS ile Farkı. Avantajları.
- **SSH Anahtar Çifti Oluşturma**: `ssh-keygen`. Parametreler. Örnek.
  - **ed25519 Anahtarı**: Tanım. Önerilen Yöntem. Örnek.
  - **RSA Anahtarı**: Tanım. Eski Yöntem. Örnek.
- **SSH Agent**: `ssh-agent`. `ssh-add`. Tanım. Örnek.
- **GitHub'a SSH Ekleme**: Adım Adım. Örnek.
- **GitLab'a SSH Ekleme**: Adım Adım. Örnek.
- **SSH Bağlantı Testi**: `ssh -T git@github.com`. Örnek.
- **Birden Fazla SSH Anahtarı**: `~/.ssh/config`. Yapılandırma. Örnek.
- **GPG ile Commit İmzalama**: Tanım. `git commit -S`. Neden Önemli? Örnek.
  - **GPG Anahtar Oluşturma**: Örnek.
  - **Git'e GPG Tanıtma**: Örnek.
  - **GitHub'a GPG Ekleme**: Örnek.
 
---
 
### Git : Cherry-Pick
- **Cherry-Pick Nedir?**: Tanım. Kullanım Senaryoları. Görselleştirme.
- **git cherry-pick**: Sözdizimi. Örnek.
  - **Tek Commit**: `git cherry-pick <hash>`. Örnek.
  - **Aralık**: `git cherry-pick A..B`. Örnek.
  - **Birden Fazla**: `git cherry-pick hash1 hash2`. Örnek.
- **Çakışma Yönetimi**: `git cherry-pick --continue`. `--abort`. Örnek.
- **`--no-commit`**: Sahneye Al Ama Commit Etme. Örnek.
- **`-x`**: Kaynak Commit Referansı Ekle. Örnek.
- **Ne Zaman Kullanılır?**: Hotfix Taşıma. Seçici Özellik Alma. Örnek.
 
---
 
### Git : Bisect
- **git bisect Nedir?**: Tanım. Binary Search ile Hata Bulma. Kullanım Senaryoları.
- **Temel Kullanım**:
  - **Başlatma**: `git bisect start`. Örnek.
  - **Kötü Commit İşaretleme**: `git bisect bad`. Örnek.
  - **İyi Commit İşaretleme**: `git bisect good <hash>`. Örnek.
  - **İlerleme**: her adımda `git bisect good/bad`. Örnek.
  - **Bitirme**: `git bisect reset`. Örnek.
- **Otomatik Bisect**: `git bisect run <script>`. Tanım. Örnek.
- **Bisect Log**: `git bisect log`. Örnek.
 
---
 
### Git : Submodule
- **Submodule Nedir?**: Tanım. Kullanım Senaryoları. Repo İçinde Repo.
- **Submodule Ekleme**: `git submodule add <url>`. Örnek.
- **`.gitmodules` Dosyası**: Tanım. İçeriği. Örnek.
- **Submodule ile Clone**: `git clone --recurse-submodules`. Örnek.
- **Mevcut Repo'ya Submodule İndir**: `git submodule init`. `git submodule update`. Örnek.
- **Submodule Güncelleme**: `git submodule update --remote`. Örnek.
- **Submodule Silme**: Adım Adım. Örnek.
- **Submodule Dezavantajları**: Tanım. Alternatifler.
 
---
 
### Git : Worktree
- **git worktree Nedir?**: Tanım. Birden Fazla Working Directory. Kullanım Senaryoları.
- **Worktree Ekleme**: `git worktree add <yol> <branch>`. Örnek.
- **Worktree Listeleme**: `git worktree list`. Örnek.
- **Worktree Silme**: `git worktree remove`. Örnek.
- **Kullanım Senaryoları**: Hotfix. Paralel Geliştirme. Örnek.
 
---
 
### Git : Reflog
- **git reflog Nedir?**: Tanım. Yerel Geçmiş Kaydı. Kullanım Senaryoları.
- **Temel Kullanım**: `git reflog`. Örnek.
- **Silinen Branch'i Kurtarma**: Adım Adım. Örnek.
- **Hard Reset'i Geri Alma**: Adım Adım. Örnek.
- **Reflog ile Checkout**: `git checkout HEAD@{n}`. Örnek.
- **Reflog Süresi**: `gc.reflogExpire`. Tanım.
 
---
 
### Git : Hooks
- **Git Hook Nedir?**: Tanım. Otomatik Tetikleme. Kullanım Senaryoları.
- **Hook Türleri**: Client-Side. Server-Side. Tablo Halinde.
- **`.git/hooks/` Klasörü**: Tanım. Örnek Dosyalar.
- **Client-Side Hook'lar**:
  - **pre-commit**: Tanım. Lint. Test Çalıştırma. Örnek.
  - **commit-msg**: Tanım. Mesaj Formatı Kontrolü. Örnek.
  - **prepare-commit-msg**: Tanım. Örnek.
  - **post-commit**: Tanım. Bildirim. Örnek.
  - **pre-push**: Tanım. Test Kontrolü. Örnek.
  - **pre-rebase**: Tanım. Örnek.
- **Server-Side Hook'lar**:
  - **pre-receive**: Tanım. Push Kısıtlama. Örnek.
  - **post-receive**: Tanım. Deploy Tetikleme. Örnek.
  - **update**: Tanım. Branch Bazlı Kısıtlama. Örnek.
- **Hook Yazma**: Bash Script. Çalıştırma İzni. `chmod +x`. Örnek.
- **Husky**: Tanım. Node.js Projelerinde Hook Yönetimi. Kurulum. Örnek.
 
---
 
### Git : Gelişmiş Log ve Arama
- **git log Gelişmiş Kullanım**:
  - **`--grep`**: Commit Mesajında Arama. Örnek.
  - **`-S`** *(Pickaxe)*: Kod İçinde Arama. Örnek.
  - **`-G`**: Regex ile Kod Arama. Örnek.
  - **`--follow`**: Yeniden Adlandırılmış Dosyayı Takip Et. Örnek.
  - **`--merges / --no-merges`**: Merge Commit Filtresi. Örnek.
  - **Özel Format**: `--pretty=format:`. Örnek.
- **git blame**: Tanım. Satır Bazlı Yazar Bilgisi. Örnek.
  - **`-L`**: Satır Aralığı. Örnek.
  - **`-w`**: Boşlukları Yoksay. Örnek.
  - **`--since`**: Tarihe Göre. Örnek.
- **git grep**: Tanım. Çalışma Dizininde Arama. Örnek.
  - **`-n`**: Satır Numarası. Örnek.
  - **`-i`**: Büyük/Küçük Harf Duyarsız. Örnek.
  - **Belirli Commit'te Arama**: `git grep "ifade" <hash>`. Örnek.
- **git shortlog**: Tanım. Yazar Bazlı Özet. Örnek.
 
---
 
### Git : Yapılandırma ve Takma Adlar (Alias)
- **git config Derinlemesi**: Tanım. Tüm Seçenekler.
  - **core.autocrlf**: Windows/Linux Satır Sonu. Tanım. Örnek.
  - **core.whitespace**: Boşluk Kontrolü. Tanım. Örnek.
  - **pull.rebase**: Varsayılan Pull Davranışı. Örnek.
  - **merge.tool**: Merge Aracı Seçimi. Örnek.
  - **diff.tool**: Diff Aracı Seçimi. Örnek.
  - **credential.helper**: Kimlik Bilgisi Önbellekleme. Örnek.
- **Alias (Takma Ad)**: Tanım. Kullanım Senaryoları.
  - **Alias Tanımlama**: `git config --global alias.isim komut`. Örnek.
  - **Yaygın Alias'lar**: `st`, `co`, `br`, `lg`. Tablo Halinde.
  - **Shell Komutlu Alias**: `!` Prefix. Örnek.
- **`.gitattributes`**: Tanım. Dosya Özellik Tanımlama. Örnek.
  - **Satır Sonu Yönetimi**: `* text=auto`. Örnek.
  - **Binary Dosya İşaretleme**: Örnek.
  - **Merge Stratejisi**: Örnek.
 
---
 
### Git : GitHub ile Çalışmak
- **GitHub Nedir?**: Tanım. GitLab ve Bitbucket ile Farkı. Tablo Halinde.
- **Repository Oluşturma**: Public vs Private. README. License. Örnek.
- **Fork**: Tanım. Kullanım Senaryosu. Adım Adım. Örnek.
- **Pull Request (PR)**: Tanım. İş Akışı. Örnek.
  - **PR Oluşturma**: Adım Adım. Örnek.
  - **PR İnceleme (Review)**: Approve. Request Changes. Comment. Örnek.
  - **PR Birleştirme**: Merge. Squash. Rebase. Farkları.
  - **Draft PR**: Tanım. Kullanım. Örnek.
- **Issue**: Tanım. Label. Milestone. Assignee. Örnek.
- **GitHub Actions**: Tanım. CI/CD. `.github/workflows/`. Örnek.
  - **Workflow Dosyası**: Tanım. Yapısı. Örnek.
  - **Otomatik Test**: Push'ta Test Çalıştırma. Örnek.
  - **Otomatik Deploy**: Tanım. Örnek.
- **GitHub Pages**: Tanım. Statik Site Yayınlama. Örnek.
- **Releases**: Tanım. Tag ile İlişkisi. Binary Ekleme. Örnek.
- **GitHub CLI (gh)**: Tanım. Kurulum. Temel Komutlar. Örnek.
  - **`gh repo clone`**: Örnek.
  - **`gh pr create`**: Örnek.
  - **`gh issue create`**: Örnek.
 
---
 
### Git : İş Akışı Modelleri
- **Git Flow**: Tanım. Branch Yapısı. Örnek.
  - **main**: Üretim Kodu.
  - **develop**: Geliştirme Dalı.
  - **feature/**: Özellik Dalları.
  - **release/**: Sürüm Hazırlık.
  - **hotfix/**: Acil Düzeltme.
  - **git-flow Aracı**: Kurulum. Komutlar. Örnek.
- **GitHub Flow**: Tanım. Adımlar. Ne Zaman Tercih Edilir? Örnek.
- **GitLab Flow**: Tanım. Environment Branch'ler. Örnek.
- **Trunk Based Development**: Tanım. Feature Flag. Kullanım. Örnek.
- **Hangi Model Ne Zaman?**: Tablo Halinde Karşılaştırma.
 
---
 
### Git : Performans ve Büyük Repolar
- **git gc**: Tanım. Çöp Toplama. Repo Temizleme. Örnek.
- **git prune**: Tanım. Ulaşılamayan Nesneleri Silme. Örnek.
- **Sığ Kopyalama (Shallow Clone)**: `--depth`. Tanım. Örnek.
- **Kısmi Kopyalama (Partial Clone)**: `--filter`. Tanım. Örnek.
- **Sparse Checkout**: Tanım. Sadece Belirli Klasörü Al. Örnek.
- **Git LFS (Large File Storage)**: Tanım. Büyük Dosya Yönetimi. Kurulum. Örnek.
  - **Dosya Takibi**: `git lfs track "*.psd"`. Örnek.
  - **`.gitattributes` ile Entegrasyon**: Örnek.
- **ORIG_HEAD, MERGE_HEAD, FETCH_HEAD**: Tanım. Kullanım Senaryoları. Örnek.
 
---
 
### Git : Güvenlik ve İyi Pratikler
- **Hassas Veri Sızıntısı**: Tanım. Senaryo. Nasıl Önlenir?
  - **git-secrets**: Tanım. Kurulum. Örnek.
  - **Geçmişten Veri Silme**: `git filter-repo`. Tanım. Örnek.
  - **.env Dosyaları**: .gitignore ile Koruma. Örnek.
- **force push Riskleri**: Tanım. Ne Zaman Tehlikeli? Korunma Yöntemleri.
- **Branch Koruma Kuralları**: GitHub. GitLab. Tanım. Ayarlar. Örnek.
- **Signed Commits**: Tanım. GPG. Önemi. Örnek.
- **Dependency Review**: Tanım. Güvenlik Taraması. Örnek.
- **İyi Pratikler Özeti**:
  > Küçük ve Sık Commit.
  > Anlamlı Commit Mesajı.
  > Branch'te Çalış.
  > main'e Direkt Push Yapma.
  > Gizli Bilgileri Asla Commit Etme.
  > PR ile Code Review Yap.
  > .gitignore'u İhmal Etme.
 
---
 
### Sonsöz
- **Bu Dokümantasyonda Ne Öğrendik**
- **İlerki Projeler**
- **Diğer Data's Books Dökümantasyonları**
- **Özel Teşekkürler**
 
---