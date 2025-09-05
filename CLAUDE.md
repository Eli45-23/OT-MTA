# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a single-file HTML application for tracking overtime hours and managing pass lists. The entire application runs client-side with data stored in browser localStorage.

## Architecture

- **Single HTML file**: `index.html` contains all HTML, CSS, and JavaScript
- **Client-side only**: No server, no build process, no dependencies
- **Data persistence**: Uses browser localStorage with these keys:
  - `pass-list-entries-v1`: Person records (name, list#, pass#)
  - `pass-list-hours-v1`: Hours by person and date
  - `ot_adjustments_v1`: Manual hour adjustments per person
  - `ot_last_change_v1::*`: Last change timestamps for ranking

## Key Components

### Data Model
- **Person**: `{ id, name, lisNumber, passNumber, createdAt, updatedAt }`
- **Hours**: Stored as `{ [personId]: { [YYYY-MM-DD]: number } }`
- **View**: Shows Fri-Mon weekends for selected month

### Main Features
1. **Person Management**: Add/edit/delete entries with list# and pass#
2. **Hours Tracking**: Input hours for weekend days (Fri-Mon)
3. **Who's Next Panel**: Live ranking by total hours (least to most)
4. **Import/Export**: CSV and JSON support
5. **Month Navigation**: View different months of weekend data

## Development Notes

- The app is designed to run by opening `index.html` directly in a browser
- All styling uses CSS custom properties for theming
- Table uses sticky positioning for frozen columns during horizontal scroll
- Hours are normalized to quarter-hour increments (0.25)
- The "Row Total" can be manually adjusted, creating an additive adjustment value

## Testing

Since this is a standalone HTML file, testing is done manually:
1. Open `index.html` in a browser
2. Test CRUD operations on person records
3. Verify hours input and totaling
4. Check import/export functionality
5. Confirm data persists after page reload