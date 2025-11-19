# Montecito Racing Website - Quick Update Guide

This guide shows you how to easily update your website's metrics and photo gallery without touching any complex code!

## 📊 Updating Impact Metrics (Donations, Races, Contributors)

**File to Edit:** `metrics-config.js`

### What Updates Automatically:
- Home page donation tracker bar
- Our Story page statistics section

### How to Update:

1. Open `metrics-config.js`
2. Change the numbers:
   ```javascript
   const METRICS = {
     totalRaised: 2847,      // ← Change this when you receive donations
     contributors: 23,       // ← Change this when you get new donors
     racesCompleted: 8,      // ← Update after each race
     goalAmount: 5000        // ← Change your fundraising goal
   };
   ```
3. Save the file
4. Refresh your website - done!

### Example Update:
**Before:**
```javascript
totalRaised: 2847,
contributors: 23,
racesCompleted: 8,
```

**After receiving $500 from 5 new donors and completing 2 races:**
```javascript
totalRaised: 3347,
contributors: 28,
racesCompleted: 10,
```

---

## 📷 Adding Photos to the Gallery

**File to Edit:** `gallery-photos.js`

### How to Add a New Photo:

1. **Upload your image** to the website folder (same folder as `index.html`)
   - Supported formats: .jpg, .jpeg, .png
   - Recommended: Keep files under 2MB

2. **Open `gallery-photos.js`**

3. **Copy this template:**
   ```javascript
   {
     image: 'your-photo-name.jpg',
     title: 'Photo Title Here',
     category: 'racing',
     date: 'December 2024'
   },
   ```

4. **Fill it in with your photo details:**
   - `image`: Your photo's filename (must match exactly!)
   - `title`: A short description of the photo
   - `category`: Choose one: `racing`, `team`, `events`, or `charity`
   - `date`: When the photo was taken

5. **Add it to the array** in `gallery-photos.js`

### Example - Adding 3 New Photos:

```javascript
const GALLERY_PHOTOS = [
  {
    image: 'IMG_6212.jpeg',
    title: 'GT3 Qualifying Session',
    category: 'racing',
    date: 'November 2024'
  },
  {
    image: 'podium-finish-imsa.jpg',      // ← New photo 1
    title: 'First Podium at IMSA Race',
    category: 'racing',
    date: 'December 2024'
  },
  {
    image: 'team-celebration.jpg',        // ← New photo 2
    title: 'Team Celebrating Win',
    category: 'team',
    date: 'December 2024'
  },
  {
    image: 'charity-event-2024.jpg',      // ← New photo 3
    title: 'Cedars-Sinai Fundraiser Event',
    category: 'charity',
    date: 'January 2025'
  },
];
```

### Photo Categories:
- `racing` - On-track racing photos
- `team` - Team photos, driver portraits
- `events` - Events, sim racing setups
- `charity` - Charity events, fundraisers

### Tips:
- ✅ Use descriptive filenames: `imsa-race-2024.jpg` instead of `IMG_1234.jpg`
- ✅ Don't forget the comma `,` after each photo object
- ✅ Make sure filenames match exactly (including uppercase/lowercase)
- ❌ Don't use spaces in filenames - use dashes instead

---

## 🚀 Publishing Updates

After making changes:

1. **Save the file** you edited (`metrics-config.js` or `gallery-photos.js`)
2. **Upload to your web host** (if using external hosting)
3. **Refresh the website** in your browser
4. **Clear cache** if changes don't appear (Ctrl+Shift+R or Cmd+Shift+R)

---

## 🆘 Troubleshooting

### Metrics not updating?
- Make sure you saved `metrics-config.js`
- Check that there are no typos in the numbers
- Refresh your browser with Ctrl+Shift+R

### Photo not showing?
- Verify the image file is uploaded to the same folder
- Check that the filename matches exactly (including .jpg/.png extension)
- Make sure there's a comma after the previous photo entry
- Open browser console (F12) to check for errors

### Photo appears but won't click?
- Make sure the image file isn't corrupted
- Try a different image format (.jpg instead of .png)

---

## 📝 Quick Checklist

**When you receive a donation:**
- [ ] Open `metrics-config.js`
- [ ] Update `totalRaised`
- [ ] Update `contributors` (if new donor)
- [ ] Save file

**When you complete a race:**
- [ ] Open `metrics-config.js`
- [ ] Update `racesCompleted`
- [ ] Save file

**When you have a new photo:**
- [ ] Upload image file to website folder
- [ ] Open `gallery-photos.js`
- [ ] Copy photo template
- [ ] Fill in image, title, category, date
- [ ] Add comma after previous entry
- [ ] Save file

---

**Need help?** Contact the team via Discord or email at montecitoracing@gmail.com
