# 🌌 Complete NASA APOD Archive for ESP32

The most comprehensive collection of NASA Astronomy Picture of the Day images optimized for ESP32 microcontrollers.

## 📊 Collection Statistics

- **Total Images**: 4
- **Resolution**: 320×240 pixels (perfect for common ESP32 TFT displays)
- **Format**: JPEG, baseline encoded for ESP32 compatibility
- **Total Size**: 76.9 KB
- **Average Size**: 19.2 KB per image
- **Date Range**: 2025-09-30 to broom
- **Compression**: 95-99% from original NASA images

## 🚀 ESP32 Usage

### Simple Random Display
```cpp
#include "esp32_all_nasa.h"

void displayRandomImage() {
  int randomIndex = random(num_nasa_images);
  
  HTTPClient http;
  http.begin(nasa_images[randomIndex].url);
  
  if (http.GET() == HTTP_CODE_OK) {
    // Your image display code here
    Serial.println(nasa_images[randomIndex].title);
  }
  
  http.end();
}
```

### Sequential Slideshow
```cpp
int current_index = 0;

void nextImage() {
  current_index = (current_index + 1) % num_nasa_images;
  // Display nasa_images[current_index]
}
```

## 🖼️ Image List

** 1.** `broom` - test (25.7 KB)
** 2.** `2025-10-01` - NGC 6960: The Witch's Broom Nebula (6.6 KB)
** 3.** `2025-10-01` - NGC 6960: The Witch's Broom Nebula (38.7 KB)
** 4.** `2025-09-30` - Comet Lemmon Brightens (5.9 KB)


## 🛠️ Technical Details

### Optimization for ESP32
- **Baseline JPEG**: Non-progressive encoding for ESP32 JPEG decoder compatibility
- **Optimal Size**: Each image under 50KB for fast WiFi download
- **Memory Efficient**: Designed for ESP32's limited RAM
- **Color Optimized**: 24-bit color depth maintained with smart compression

### GitHub Pages URLs
All images are hosted on GitHub Pages and accessible via HTTPS:
```
https://roccoss39.github.io/nasa.github.io/nasa-images/[filename].jpg
```

### Download Performance
- **Average download time**: 2-5 seconds on typical WiFi
- **Memory usage**: ~50KB RAM for largest images
- **Display time**: <1 second with TJpg_Decoder

## 📁 Repository Structure

```
/
├── index.html              # Web gallery
├── nasa-images/           # Image directory (4 files)
│   ├── nasa_2025-10-01_NGC_6960.jpg
│   ├── nasa_2025-09-30_Comet_Lemmon.jpg
│   └── ...
├── esp32_all_nasa.h       # ESP32 code
└── README.md              # This file
```

## 🌌 About NASA APOD

NASA's Astronomy Picture of the Day (APOD) presents a different astronomical image each day, showcasing the universe's beauty and mystery. This collection represents the finest space imagery optimized for embedded systems.

## 📄 License

Images courtesy of NASA APOD. See individual image credits on the NASA APOD website.

---

**Generated**: 2025-11-04 13:03:00  
**Total Images**: 4  
**ESP32 Ready**: ✅  
**GitHub Pages**: ✅  
