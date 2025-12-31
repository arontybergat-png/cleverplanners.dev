# What to Fix First - Prioritized Action Plan

## 🎯 Start Here: Quick Wins (1-2 hours)

These fixes will have **immediate visual impact** and make the site feel more cohesive:

### 1. **Standardize Background Colors** ⚡ (15 minutes)
**Problem:** `results.html` uses `#faf8f4` instead of `var(--cream) #fbf6ed`
**Fix:** Change one line in `results.html`
**Impact:** High - immediate visual consistency

### 2. **Fix Border Radius Inconsistency** ⚡ (5 minutes)
**Problem:** `vendors.html` uses `--radius: 24px` while others use `20px`
**Fix:** Change `--radius: 24px` to `--radius: 20px` in `vendors.html`
**Impact:** Medium - subtle but noticeable

### 3. **Standardize Logo Links** ⚡ (10 minutes)
**Problem:** Logos link to different pages (index.html, plan.html, dashboard.html)
**Fix:** Standardize to: Logo → `index.html` (or dashboard if logged in)
**Impact:** High - better navigation consistency

### 4. **Fix "Forgot Password" Links** ⚡ (30 minutes)
**Problem:** Links to `#` (broken)
**Fix:** Create simple `forgot-password.html` page
**Impact:** High - fixes broken functionality

### 5. **Add Profile Dropdown to Missing Pages** ⚡ (20 minutes)
**Problem:** Missing on `vendors.html` and `checklists.html`
**Fix:** Copy profile dropdown code from `dashboard.html`
**Impact:** Medium - better UX for logged-in users

**Total Time: ~1.5 hours | Impact: Very High**

---

## 🔥 Next: Critical User Flow Fixes (2-3 hours)

These fix broken or confusing user journeys:

### 6. **Fix Checklist Event Type Links** (1 hour)
**Problem:** `checklists.html` shows event types but links go nowhere
**Fix Options:**
- **Option A (Quick):** Link to `plan.html` with event type pre-selected
- **Option B (Better):** Create simple checklist detail pages
**Recommendation:** Start with Option A, enhance later

### 7. **Connect Vendor Search to Results** (1 hour)
**Problem:** Unclear how `vendors.html` search connects to `results.html`
**Fix:** Ensure search redirects to `results.html?search=query`
**Impact:** High - fixes core functionality

### 8. **Ensure Plan → Results Transition** (30 minutes)
**Problem:** `plan.html` Step 6 may not properly link to `results.html`
**Fix:** Verify and fix the transition
**Impact:** High - critical user flow

**Total Time: ~2.5 hours | Impact: Critical**

---

## 🎨 Then: Design System Standardization (3-4 hours)

These create a unified design language:

### 9. **Create Master Color Palette** (1 hour)
**Problem:** Color variables defined differently across pages
**Fix:** 
1. Create `design-tokens.css` with all variables
2. Include it in all pages
3. Remove duplicate `:root` declarations
**Impact:** Very High - foundation for consistency

### 10. **Standardize Shadow System** (30 minutes)
**Problem:** Multiple shadow definitions
**Fix:** Create consistent shadow scale in design tokens
**Impact:** Medium - subtle polish

### 11. **Create Button Component System** (1 hour)
**Problem:** Button styles vary
**Fix:** Define `.btn-primary`, `.btn-secondary`, `.btn-ghost` classes
**Impact:** High - visual consistency

### 12. **Standardize Header Component** (1.5 hours)
**Problem:** Different header styles on every page
**Fix:** Create consistent header HTML/CSS structure
**Impact:** Very High - major visual consistency

**Total Time: ~4 hours | Impact: Very High**

---

## 📋 After That: Missing Pages (4-5 hours)

### 13. **Create Forgot Password Page** (1 hour)
- Simple form with email input
- Success message
- Link back to login

### 14. **Create Checklist Detail Pages** (3-4 hours)
- Template for each event type
- Checklist items
- Check/uncheck functionality
- Save to localStorage

**Total Time: ~5 hours | Impact: High**

---

## 🚀 Recommended Order of Execution

### **Phase 1: Quick Wins (Today - 1.5 hours)**
Do items 1-5 above. These are fast and have immediate impact.

### **Phase 2: Critical Flows (Tomorrow - 2.5 hours)**
Do items 6-8. These fix broken functionality.

### **Phase 3: Design System (This Week - 4 hours)**
Do items 9-12. These create the foundation for consistency.

### **Phase 4: Missing Pages (Next Week - 5 hours)**
Do items 13-14. These complete the feature set.

---

## 💡 Pro Tip: Start with Visual Consistency

The **fastest way to make the site feel polished** is to:
1. Fix background colors (5 min)
2. Fix border radius (5 min)
3. Standardize logo links (10 min)

**Total: 20 minutes for immediate visual improvement!**

Then tackle the user flow fixes, then the design system.

---

## 🎯 My Recommendation: Start Here

**Begin with these 3 fixes (20 minutes total):**
1. Standardize background colors
2. Fix border radius
3. Standardize logo links

Then move to:
4. Fix "Forgot Password" link
5. Add profile dropdowns

This gives you **maximum impact in minimum time**.

