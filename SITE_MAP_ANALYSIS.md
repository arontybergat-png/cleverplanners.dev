# Site Map Analysis - CleverPlanners

## 📋 Existing Pages Mapping

### ✅ Pages That Exist

| Site Map Node | File Name | Status | Notes |
|--------------|-----------|--------|-------|
| **Homepage** | `new plan.html` | ✅ EXISTS | Main landing page with hero section |
| **Questionairee Page** | `plan.html` | ✅ EXISTS | Multi-step questionnaire wizard |
| **Results Page** | `results.html` | ✅ EXISTS | Shows vendor recommendations after questionnaire |
| **Vendor Search Page** | `vendors.html` | ✅ EXISTS | Search and browse vendors |
| **Vendor Onboarding Questioneree** | `vendor-onboarding.html` | ✅ EXISTS | Vendor sign-up form |
| **Test Page** | `test.html` | ✅ EXISTS | The Knot marketplace clone (test) |

### ❌ Missing Pages

| Site Map Node | Priority | Description |
|--------------|----------|-------------|
| **Login & Sign Up** | 🔴 HIGH | User authentication page (needed for Results → Personal Page flow) |
| **Vendor Sign up & Login** | 🔴 HIGH | Separate vendor authentication page |
| **Full Vendor Page** | 🔴 HIGH | Individual vendor detail/profile page (linked from Search and Results) |
| **Personal Page** | 🔴 HIGH | User's personal dashboard/plan page (after login from Results) |
| **User Personal Page** | 🟡 MEDIUM | Alternative user profile page (from Search flow) |
| **Vendor Dashboard** | 🟡 MEDIUM | Vendor's main dashboard after login |
| **Vendor Settings** | 🟢 LOW | Vendor account settings page |
| **Settings Personal Info** | 🟢 LOW | User account settings page |
| **Admin Dashboard** | 🟢 LOW | Admin panel for managing the platform |

### 🔗 Navigation Connections Analysis

#### From Homepage (`new plan.html`):
- ✅ → Vendors (link exists in nav)
- ✅ → Search Vendors (CTA exists)
- ✅ → Begin Here (CTA exists, links to `plan.html`)
- ❌ → Login & Sign Up (missing)
- ❌ → Admin Dashboard (missing)

#### From Questionnaire (`plan.html`):
- ✅ → Results Page (works correctly)

#### From Results Page (`results.html`):
- ❌ → Login & Sign Up (missing - needed to save plan)
- ❌ → Full Vendor Page (missing - needed to view vendor details)
- ❌ → Personal Page (missing - where users go after login)

#### From Vendor Search (`vendors.html`):
- ❌ → Full Vendor Page (missing - needed to view vendor details)
- ❌ → User Personal Page (missing - user profile from search flow)

#### From Vendor Onboarding (`vendor-onboarding.html`):
- ❌ → Vendor Sign up & Login (missing - needed after onboarding)
- ❌ → Vendor Dashboard (missing - where vendors go after login)

---

## 🎯 Implementation Plan

### Phase 1: Critical Pages (User Flow Blockers) 🔴

#### 1. **Login & Sign Up** (`login.html`)
**Priority:** CRITICAL
**Purpose:** User authentication for saving plans and accessing personal dashboard
**Connections:**
- From: Homepage, Results Page
- To: Personal Page
**Features Needed:**
- Login form (email/password)
- Sign up form (email, password, name)
- "Forgot password" link
- Social login options (optional)
- Remember me checkbox
- Redirect to Personal Page after login

#### 2. **Full Vendor Page** (`vendor-detail.html` or `vendor.html`)
**Priority:** CRITICAL
**Purpose:** Detailed vendor profile page
**Connections:**
- From: Vendor Search Page, Results Page
- To: Personal Page (add to plan), Contact vendor
**Features Needed:**
- Vendor hero image/gallery
- Vendor name, category, location
- Rating and reviews
- Pricing information
- Services offered
- Availability calendar
- Contact form/button
- "Add to Plan" button
- Social media links
- Portfolio/images
- Map location

#### 3. **Personal Page** (`dashboard.html`)
**Priority:** CRITICAL
**Purpose:** User's personal dashboard showing their saved plan
**Connections:**
- From: Login & Sign Up (after Results), Login & Sign Up (from Search)
- To: Settings Personal Info, Full Vendor Page, Results Page
**Features Needed:**
- Saved vendors list
- Budget tracker
- Event details (date, location, type)
- Progress checklist
- "Continue Planning" button
- Edit/remove vendors
- Share plan option
- Export plan (PDF?)

#### 4. **Vendor Sign up & Login** (`vendor-login.html`)
**Priority:** HIGH
**Purpose:** Vendor authentication
**Connections:**
- From: Vendors page, Vendor Onboarding
- To: Vendor Dashboard
**Features Needed:**
- Vendor login form
- Vendor sign up form
- Link to Vendor Onboarding
- "Forgot password" link

#### 5. **Vendor Dashboard** (`vendor-dashboard.html`)
**Priority:** HIGH
**Purpose:** Vendor's main control panel
**Connections:**
- From: Vendor Sign up & Login
- To: Vendor Settings, Full Vendor Page (edit)
**Features Needed:**
- Dashboard overview (views, inquiries, bookings)
- Profile completion status
- Recent inquiries/messages
- Quick stats (views, favorites, inquiries)
- Edit profile button
- View public profile link
- Settings link

### Phase 2: Secondary Pages (Enhanced Functionality) 🟡

#### 6. **User Personal Page** (`user-profile.html`)
**Priority:** MEDIUM
**Purpose:** Alternative user profile from search flow
**Note:** Could potentially merge with Personal Page if they serve the same purpose

#### 7. **Settings Personal Info** (`settings.html` or `account-settings.html`)
**Priority:** MEDIUM
**Purpose:** User account settings
**Connections:**
- From: Personal Page
**Features Needed:**
- Edit profile information
- Change password
- Email preferences
- Notification settings
- Delete account option

#### 8. **Vendor Settings** (`vendor-settings.html`)
**Priority:** MEDIUM
**Purpose:** Vendor account and profile settings
**Connections:**
- From: Vendor Dashboard
**Features Needed:**
- Edit business information
- Update services/pricing
- Manage photos/portfolio
- Availability settings
- Change password
- Account settings

### Phase 3: Admin & Advanced Features 🟢

#### 9. **Admin Dashboard** (`admin.html` or `admin-dashboard.html`)
**Priority:** LOW
**Purpose:** Platform administration
**Connections:**
- From: Homepage (admin only)
**Features Needed:**
- User management
- Vendor management
- Content moderation
- Analytics
- System settings

---

## 📝 Recommended File Naming Convention

```
login.html                    - User login/signup
vendor-login.html             - Vendor login/signup
vendor-detail.html            - Full vendor page (or vendor.html)
dashboard.html                - User's personal plan dashboard
user-profile.html             - User profile page (if different from personal-page)
vendor-dashboard.html         - Vendor dashboard
vendor-settings.html          - Vendor settings
settings.html                 - User account settings
admin-dashboard.html          - Admin panel
```

---

## 🚀 Suggested Implementation Order

1. **Login & Sign Up** - Unblocks user flow from Results page
2. **Full Vendor Page** - Essential for viewing vendor details
3. **Personal Page** - Where users land after login to see their plan
4. **Vendor Sign up & Login** - Enables vendor access
5. **Vendor Dashboard** - Vendor control panel
6. **Settings pages** - Account management
7. **Admin Dashboard** - Platform management

---

## 🔄 Navigation Updates Needed

### Update `new plan.html`:
- Add link to `login.html` in header
- Ensure "Vendors" link works (points to `vendors.html`)

### Update `results.html`:
- Add "Login to Save Plan" button → `login.html`
- Update vendor card links → `vendor-detail.html`
- Add "View Full Profile" buttons

### Update `vendors.html`:
- Update vendor card links → `vendor-detail.html`
- Add "Login" link in header → `login.html`

### Update `vendor-onboarding.html`:
- Add "Already have an account? Login" link → `vendor-login.html`
- After form submission, redirect to `vendor-login.html` or `vendor-dashboard.html`

### Update `plan.html`:
- Ensure it properly links to `results.html` after completion

---

## ✅ Next Steps

1. Review this analysis
2. Prioritize which pages to build first
3. Create detailed specifications for each page
4. Begin implementation starting with Phase 1 pages





