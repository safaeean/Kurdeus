# 📥 فایل: https://github.com/niklasvh/html2canvas/releases/download/v1.4.1/html2canvas.min.js?v2

**حجم:** 0.19 MB
**تعداد تکه‌ها:** 2 تکه (هر تکه 100 KB)

---

## 🧩 تکه‌های فایل

لطفاً این فایل README را در یک ریپازیتوری گیت‌هاب قرار دهید.

<img src="https://super-river-0ee1.info-mihandesign.workers.dev/chunk0.svg?file=https%3A%2F%2Fgithub.com%2Fniklasvh%2Fhtml2canvas%2Freleases%2Fdownload%2Fv1.4.1%2Fhtml2canvas.min.js%3Fv2" alt="chunk1"/>

<img src="https://super-river-0ee1.info-mihandesign.workers.dev/chunk1.svg?file=https%3A%2F%2Fgithub.com%2Fniklasvh%2Fhtml2canvas%2Freleases%2Fdownload%2Fv1.4.1%2Fhtml2canvas.min.js%3Fv2" alt="chunk2"/>

---

### 🔧 اسکریپت خودکار برای لینوکس

```bash
#!/bin/bash

WORKER_URL="https://super-river-0ee1.info-mihandesign.workers.dev"
ENCODED_LINK="https%3A%2F%2Fgithub.com%2Fniklasvh%2Fhtml2canvas%2Freleases%2Fdownload%2Fv1.4.1%2Fhtml2canvas.min.js%3Fv2"
TOTAL_CHUNKS=2

echo "Downloading $TOTAL_CHUNKS chunks..."

for i in $(seq 0 $((TOTAL_CHUNKS - 1))); do
  echo "  Chunk $i/$((TOTAL_CHUNKS - 1))"
  curl -s "$WORKER_URL/chunk$i.svg?file=$ENCODED_LINK" | \
    grep -oP '(?<=<text[^>]*>)[^<]+' | \
    grep -v "Chunk" | grep -v "end of chunk" | \
    tr -d '
' >> chunks.b64
done

echo "Decoding and restoring file..."
base64 -d chunks.b64 > restored_file
rm chunks.b64

echo "✅ File saved as: restored_file"
```

> ⚠️ **توجه:** لینک‌های دانلود فقط 10 دقیقه معتبر هستند.
