# Rent Fair Value

**Know if you're overpaying for rent in London — instantly.**

<p align="center">
  <img src="icons/icon128.png" alt="Rent Fair Value Logo" width="128" height="128">
</p>

<p align="center">
  <a href="#installation">
    <img src="https://img.shields.io/badge/Chrome-Extension-4285F4?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Chrome Extension">
  </a>
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="MIT License">
  <img src="https://img.shields.io/badge/100%25-Client--Side-orange?style=for-the-badge" alt="Client-Side">
</p>

---

## What It Does

When you browse rental listings on Rightmove, Knight Frank, Chestertons, or Savills, this extension automatically shows you:

- **Fair Market Value** — ML-predicted rent based on 10,000+ London listings
- **Premium/Discount** — How much above or below market rate the asking price is
- **Comparable Properties** — Similar rentals in the same area

<p align="center">
  <img src="icons/store-screenshot-1.png" alt="Extension showing fair value sidebar on a Rightmove listing" width="600">
</p>

---

## Key Features

| | Feature | Description |
|---|---------|-------------|
| **ML-Powered** | XGBoost model trained on 10,000+ London rentals with 91% accuracy |
| **Instant Results** | Fair value appears in seconds — no waiting for API calls |
| **100% Private** | All processing happens in your browser. No data leaves your device. |
| **Compare Properties** | Side-by-side comparison of similar listings in the area |
| **Works Offline** | The model runs locally — no internet required after install |

---

## Installation

### Option 1: Chrome Web Store (Recommended)

<!-- When published, replace with actual Chrome Web Store link -->
Coming soon to the Chrome Web Store.

### Option 2: Manual Install (3 minutes)

<details>
<summary><strong>Click to expand installation steps</strong></summary>

#### Step 1: Download the Extension

1. Click the green **Code** button at the top of this page
2. Select **Download ZIP**
3. Unzip the downloaded file
4. Navigate to the `scrapy_project/chrome-extension` folder

#### Step 2: Load in Chrome

1. Open Chrome and go to `chrome://extensions`
2. Enable **Developer mode** (toggle in the top right corner)
3. Click **Load unpacked**
4. Select the `chrome-extension` folder you unzipped

#### Step 3: Start Browsing

1. Go to any property listing on [Rightmove](https://www.rightmove.co.uk), [Knight Frank](https://www.knightfrank.co.uk), [Chestertons](https://www.chestertons.co.uk), or [Savills](https://www.savills.com)
2. The fair value sidebar appears automatically on the right side of the page

</details>

---

## Supported Websites

| Website | Status |
|---------|--------|
| [Rightmove](https://www.rightmove.co.uk) | Fully Supported |
| [Knight Frank](https://www.knightfrank.co.uk) | Fully Supported |
| [Chestertons](https://www.chestertons.co.uk) | Fully Supported |
| [Savills](https://www.savills.com) | Fully Supported |

---

## Privacy & Permissions

**Your data stays on your device.** This extension:

- Runs entirely in your browser — no external API calls
- Does not collect, store, or transmit any personal data
- Does not track your browsing history
- Is completely open source — inspect the code yourself

### Why These Permissions?

| Permission | Why It's Needed |
|------------|-----------------|
| `activeTab` | Read property details from the current listing page |
| `storage` | Save your preferences locally |
| Host permissions | Access property images for floor plan analysis |

[Read our full Privacy Policy](PRIVACY_POLICY.md)

---

## How It Works

```
You visit a rental listing
        ↓
Extension extracts property details (beds, location, size)
        ↓
ML model calculates fair market value
        ↓
You see if the rent is above or below market rate
```

**Technical details:** The extension uses an XGBoost model trained on 10,000+ London rental listings. It extracts 143 features including location, size, bedrooms, and property type to predict fair market rent with 91% accuracy.

---

## FAQ

<details>
<summary><strong>Is this extension free?</strong></summary>

Yes, completely free and open source.
</details>

<details>
<summary><strong>Does it work outside London?</strong></summary>

Currently, the model is trained only on London rental data. Results for properties outside London may not be accurate.
</details>

<details>
<summary><strong>How accurate are the estimates?</strong></summary>

The model achieves 91% accuracy (R² score: 0.908) with a median error of 4.5%. For most properties, the estimate is within £100 of a fair market value.
</details>

<details>
<summary><strong>Why does it need access to multiple websites?</strong></summary>

The extension needs to read property details from listing pages to calculate fair value. It only activates on the four supported property websites.
</details>

<details>
<summary><strong>Can I use this on Firefox/Safari/Edge?</strong></summary>

Currently, only Chrome (and Chromium-based browsers like Edge, Brave, Arc) are supported.
</details>

<details>
<summary><strong>The extension isn't showing on a listing. What do I do?</strong></summary>

1. Make sure you're on a property detail page (not search results)
2. Try refreshing the page
3. Check that the extension is enabled in `chrome://extensions`
4. If the issue persists, [open an issue](https://github.com/kavanaghpatrick/rent-fair-value/issues)
</details>

---

## Support

- **Bug reports:** [Open an issue](https://github.com/kavanaghpatrick/rent-fair-value/issues)
- **Feature requests:** [Open an issue](https://github.com/kavanaghpatrick/rent-fair-value/issues)

---

## License

MIT License — free to use, modify, and distribute.

---

<p align="center">
  <strong>Stop overpaying for rent.</strong><br>
  <a href="#installation">Install Rent Fair Value →</a>
</p>
