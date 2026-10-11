# 📚 Kurulum Rehberi

## Adım 1: Git Yükle

### Windows
1. https://git-scm.com/download/win adresine git
2. İndirilen dosyayı çalıştır
3. Kurulumu tamamla (varsayılan ayarlar uygun)
4. Terminali yeniden başlat

### Mac
```bash
brew install git
```

### Linux
```bash
sudo apt-get install git
```

## Adım 2: Repository'yi Klone Et

```bash
cd C:\Users\Asus
git clone https://github.com/alibaklaea/claude-skills.git
cd claude-skills
```

## Adım 3: GitHub'a Bağlanmayı Ayarla

### Kimlik Bilgilerini Ayarla
```bash
git config --global user.name "Senin Adın"
git config --global user.email "senin-email@example.com"
```

### SSH Key Oluştur (İsteğe Bağlı, Güvenli Yöntem)
```bash
ssh-keygen -t ed25519 -C "senin-email@example.com"
```

## Adım 4: Claude Code'a Skills'i Ekle

### Yöntem 1: .claude/skills Klasörü Kullan
1. Claude Code'u aç
2. Settings → Skills
3. "Add Skill" tıkla
4. `.claude/skills/` klasörünü seç
5. Yüklemek istediğin skill'i seç

### Yöntem 2: Manuel Entegrasyon
Eğer skill .claude klasöründe zaten varsa:
1. Claude Code'u yeniden başlat
2. Skill'ler otomatik olarak yüklenecek

## Adım 5: Değişiklikleri GitHub'a Push Et

```bash
# Durumu kontrol et
git status

# Tüm dosyaları ekle
git add .

# Commit yap
git commit -m "15 Claude skill'i ekle"

# GitHub'a push et
git push -u origin main
```

## Sorun Giderme

### "git: command not found" Hatası
**Çözüm:** Git'i yüklediğinden emin ol ve PowerShell'i yeniden başlat

### "Permission denied" Hatası
**Çözüm:** GitHub SSH key'ini ayarla veya Personal Access Token kullan

### Conflicted Files
```bash
# Değişiklikleri git tarafından koru
git merge --theirs .

# Sonra push et
git push
```

## Ek Yardım

- GitHub Rehberi: https://docs.github.com
- Git Cheat Sheet: https://git-scm.com/docs
- Claude Code Docs: https://claude.ai/code

---

**Herhangi sorun yaşarsan, GitHub Issues'te yardım isteyebilirsin!**
