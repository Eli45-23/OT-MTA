# OT-MTA Overtime Management System

A client-side overtime tracking application for managing worker schedules, hours, and shift assignments.

## Features

- 📝 **Worker Management**: Track workers with list numbers and pass numbers
- ⏰ **Shift Scheduling**: 5 weekend shifts (Fri 10p-Mon 6a coverage)
- 🎯 **Fair Assignment**: Hour-based ranking with provisional worker support
- 📱 **Mobile Responsive**: Optimized for phones and tablets
- 💾 **Offline Ready**: All data stored locally in browser
- 🔒 **Privacy First**: No server, no tracking, data stays on your device

## Deployment

### Render.com (Recommended)

1. Fork/clone this repository
2. Connect to [Render.com](https://render.com)
3. Create new "Static Site"
4. Deploy automatically with zero configuration

### Other Static Hosts

Works on any static hosting service:
- GitHub Pages
- Netlify  
- Vercel
- AWS S3
- Surge.sh

## Usage

1. **Add Workers**: Enter names with list numbers (use "P123" for provisional workers)
2. **Manage Hours**: Track weekend overtime hours across 5 shifts
3. **Fair Assignment**: System ranks by lowest hours first, respects seniority
4. **Export Data**: Download worker data as CSV or JSON

## Technical Details

- **Pure HTML/CSS/JS**: No build process required
- **LocalStorage**: Data persists in browser only
- **Responsive Design**: Mobile-first with desktop support
- **Offline Capable**: Works without internet connection

## Data Storage

All data is stored locally in your browser's localStorage:
- Worker records and hours
- Shift assignments and refusals  
- Adjustment tracking
- No server or database required

## License

MIT License - Use freely for managing overtime schedules.