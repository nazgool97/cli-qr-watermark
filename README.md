# cli-qr-watermark


**cli-qr-watermark** is a tiny yet powerful CLI tool that **adds a semi-transparent QR-code on top of a batch of images with a single command**.  
Perfect for photographers, marketers, Telegram-channel owners, or anyone who needs to watermark hundreds of photos in seconds.

---

## ⚡ Quick Start

### 1. Install
```bash
pip install cli-qr-watermark
```

### 2. Minimal Example
```

qrmark "photos/*.jpg" --url https://t.me/YOUR_CHANNEL
```

📖 Usage

Full Syntax
```
qrmark PATTERN [options]
```
| Parameter        | Default               | Description                                                    |
| ---------------- | --------------------- | -------------------------------------------------------------- |
| `PATTERN`        | —                     | Glob pattern of files (e.g. `"*.jpg"` or `"~/pics/**/*.png"`). |
| `--url`          | `https://example.com` | Link to encode in the QR-code.                                 |
| `--opacity`      | `0.4`                 | Opacity of the QR-code, 0 (invisible) to 1 (fully opaque).     |
| `--size`         | `128`                 | Side length of the QR-code in pixels.                          |
| `--output`, `-o` | `./ready`             | Directory where processed files will be saved.                 |




Examples

QR-code in the top-left corner, semi-transparent
```
qrmark "photos/*.jpg" --url https://t.me/YOUR_CHANNEL --opacity 0.3 --position tl
```

Custom output folder
```
qrmark "~/Downloads/*.jpeg" -o ~/Desktop/watermarked --size 200
```



🔧 Install from Source (for developers)
```
git clone https://github.com/nazgool97/cli-qr-watermark.git
cd cli-qr-watermark
python -m venv venv
source venv/bin/activate
pip install -e .
```
🧪 Tests
pip install pytest
pytest

📦 System Requirements
Python 3.9+
Pillow, qrcode, click, rich (installed automatically via pip).

🐞 Bugs & Feature Requests
Open an Issue on GitHub:
https://github.com/nazgool97/cli-qr-watermark/issues

📜 License
MIT © nazgool97
