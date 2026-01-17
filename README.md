# Rent Fair Value

**Know if you're overpaying for rent in London — instantly.**

<p align="center">
  <a href="https://github.com/kavanaghpatrick/rent-fair-value/releases/latest/download/rent-fair-value-v1.0.0.zip">
    <img src="https://img.shields.io/badge/⬇_Download_Extension-22c55e?style=for-the-badge" alt="Download Extension">
  </a>
</p>

---

## What It Does

A Chrome extension that shows you the **fair market rent** for any London property listing.

When you visit a rental on Rightmove, Knight Frank, Chestertons, or Savills, a sidebar appears showing whether the asking rent is fair.

### Fair Value Sidebar

The sidebar shows the ML-predicted fair rent and how the asking price compares to market rate.

<p align="center">
  <img src="icons/store-screenshot-1.png" alt="Sidebar showing fair value estimate on a Rightmove listing" width="600">
</p>

### Compare Similar Properties

Click "Compare with Similar Properties" to see a side-by-side view of comparable rentals in the same area — same bedrooms, similar size, and nearby location.

<p align="center">
  <img src="icons/store-screenshot-2.png" alt="Comparison view of similar properties" width="600">
</p>

---

## Install (2 minutes)

1. **[Download the ZIP](https://github.com/kavanaghpatrick/rent-fair-value/releases/latest/download/rent-fair-value-v1.0.0.zip)**
2. Unzip the file
3. Open Chrome → `chrome://extensions`
4. Enable **Developer mode** (top right toggle)
5. Click **Load unpacked** → select the unzipped folder
6. Visit any rental listing on a supported site

### Supported Sites

- [Rightmove](https://www.rightmove.co.uk)
- [Knight Frank](https://www.knightfrank.co.uk)
- [Chestertons](https://www.chestertons.co.uk)
- [Savills](https://www.savills.com)

---

## How It Works

1. **Extract** — When you visit a property listing, the extension reads the property details (bedrooms, bathrooms, size, postcode) from the page
2. **Predict** — An XGBoost model trained on 10,000+ London rentals predicts fair market rent (91% accuracy, median error 4.5%)
3. **Compare** — The model finds similar properties in the same area to validate the estimate

The model considers:
- Location (postcode district)
- Property size (sqft, extracted from floorplans via OCR if needed)
- Bedrooms and bathrooms
- Property type (flat, house, studio, penthouse)
- Listing agent

All processing runs locally in your browser — no data is sent to any server.

---

## Privacy

- No data collection
- No tracking
- No external API calls
- Open source — inspect the code yourself

[Full Privacy Policy](PRIVACY_POLICY.md)

---

## Support

[Open an issue](https://github.com/kavanaghpatrick/rent-fair-value/issues) for bugs or feature requests.
