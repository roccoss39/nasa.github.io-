# 🚀 GitHub Pages Setup - Proste instrukcje

## 📋 Kroki:

### 1. Stwórz repo na GitHub
- Idź na github.com
- New Repository
- Nazwa: **USERNAME.github.io** (twoja nazwa GitHub)
- ✅ Public
- ✅ Add README

### 2. Sklonuj i dodaj pliki
```bash
git clone https://github.com/USERNAME/USERNAME.github.io.git
cd USERNAME.github.io

# Skopiuj pliki NASA
cp -r github_pages_nasa/* .
ls nasa-images/  # 4 obrazków

# Git push
git add .
git commit -m "Add NASA images for ESP32"
git push
```

### 3. Włącz GitHub Pages
- GitHub repo → Settings → Pages  
- Source: **Deploy from a branch**
- Branch: **main**
- Save

### 4. Zaktualizuj ESP32
- Otwórz `esp32_github_simple.h`
- Zamień **USERNAME** na swoją nazwę GitHub
- Skopiuj do projektu ESP32

## 🎯 Finalne URL:
`https://USERNAME.github.io/nasa-images/nazwa_obrazka.jpg`

## ✅ Gotowe!
Po 5-10 minutach obrazki będą dostępne globalnie!
