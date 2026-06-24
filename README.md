# China Travel Wrapped

A **Spotify Wrapped-style** travel budget dashboard for your China overland trip. Every yuan tracked, every city counted.

## 🎨 Features

- **Live GitHub Auto-Load**: Dashboard automatically pulls the latest `transactions.csv` from this repo
- **Animated Stat Cards**: Gradient-themed cards with scroll-triggered reveals and number counters
- **Rich Analytics**:
  - Daily burn rate chart
  - Category breakdown with donut chart
  - City-by-city spending analysis
  - Food, accommodation, and transport deep-dives
  - Spending pace tracker with running totals
  - Day-of-week spending patterns
  - Payment method breakdown
  - Expandable daily transaction log

- **Drag-and-Drop CSV Upload**: Update the dashboard with a new CSV anytime
- **Responsive Design**: Works on mobile, tablet, and desktop
- **Dark Mode**: Premium Spotify Wrapped aesthetic

## 📊 Data Format

The dashboard expects a `transactions.csv` with these columns:

```
#, Date, Merchant, CNY, USD, Category, Payment, City, Expense Type, Notes
```

**Example:**
```
1, 2026-06-05 00:00:00, ESIMDOG, -47.18, -6.98, Shopping, Apple Pay, China, Irregular, data eSIM
2, 2026-06-07 00:00:00, Trip.com (USD), -60.10, -8.89, Accommodation, Apple Pay, Shenzhen, Core, 1 night Jun 8
```

### Key Rules:
- **Date**: YYYY-MM-DD format (time component is optional)
- **USD**: Negative values for expenses, positive for refunds
- **City**: Use actual city names (Shenzhen, Guilin, etc.) or "China" for trip-wide costs (SIM, VPN, centrally-booked rail)
- **Category**: Food, Accommodation, Transport, Intercity Transport, Activities, Shopping, etc.

## 🚀 Deployment

### Vercel (Recommended)
1. Connect this GitHub repo to Vercel
2. Vercel will auto-deploy on every push to `main`
3. No build step needed — it's a static site

### Manual Deployment
- Copy the `index.html` and `assets/` folder to any static hosting (GitHub Pages, Netlify, etc.)

## 📝 Updating Your Data

1. **Push to GitHub**: Update `transactions.csv` in this repo and push
2. **Dashboard auto-refreshes**: The live dashboard will pull the new data on next visit
3. **Or upload manually**: Use the drag-and-drop CSV uploader on the dashboard

## 🎯 Supported Categories

- **Food**: Meals, snacks, restaurants
- **Accommodation**: Hotels, hostels, stays
- **Transport**: Local metro, buses, bikes
- **Intercity Transport**: Trains, flights between cities
- **Activities**: Tours, experiences, attractions
- **Shopping**: Gear, souvenirs, supplies
- **Personal Care**: Haircuts, laundry, medical
- **Subscription**: Memberships, apps
- **Laundry**: Laundry services

## 🛠️ Tech Stack

- **Frontend**: React 19 + Tailwind CSS 4
- **Charts**: Recharts
- **CSV Parsing**: Custom parser with quoted field support
- **Hosting**: Vercel (static)

## 📱 Mobile-First Responsive

- Hero section adapts to all screen sizes
- Cards stack vertically on mobile
- Charts reflow for readability
- Touch-friendly drag-and-drop

## 🌍 Cities Included

Shenzhen → Guangzhou → Guilin → Yangshuo → Kunming → Pu'er

(Customize by adding your own cities to `transactions.csv`)

## 💡 Tips

- **Trip-wide costs**: Use "China" as the city for SIM cards, VPNs, and centrally-booked train tickets
- **Refunds**: Use positive USD values for refunds (e.g., hostel deposit returns)
- **Notes**: Add context in the Notes column (e.g., "3 nights", "group dinner")
- **Refresh**: Hit "Refresh from GitHub repo" button to pull latest data without uploading

## 📄 License

MIT — feel free to fork and customize for your own travels!

---

**Built with ❤️ for travel budgeting**
