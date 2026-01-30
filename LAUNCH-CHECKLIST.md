# 🚀 Launch Checklist for PickleballAddicts.com

## CRITICAL - Must Do Before Launch

### 1. Add Images (REQUIRED) ⚠️
**Status**: 🔴 NOT STARTED

Currently, all destination pages reference images that don't exist yet. The site will work but images won't display.

**Action Items:**
- [ ] Download 7 high-quality images (1400x600px) for each destination
- [ ] Optimize images to <200KB each using TinyPNG
- [ ] Save to: `images/destinations/` with exact filenames:
  - `jw-marriott-phoenix.jpg`
  - `naples-florida.jpg`
  - `sandals-caribbean.jpg`
  - `palm-springs.jpg`
  - `omni-amelia-island.jpg`
  - `turtle-bay-oahu.jpg`
  - `san-diego-coronado.jpg`

**Where to get images:**
- Unsplash.com (search: "[destination name] pickleball" or "[destination name] resort")
- Pexels.com
- Resort websites (request permission)

**Time estimate**: 1-2 hours

---

### 2. Set Up Affiliate Accounts
**Status**: 🔴 NOT STARTED

All affiliate links currently have `PLACEHOLDER` - they need your actual affiliate IDs.

**Action Items:**
- [ ] Sign up for Booking.com Partner Program (partners.booking.com)
- [ ] Wait for approval (usually 24-48 hours)
- [ ] Get your affiliate ID (format: `aid=XXXXXXX`)
- [ ] Find & replace all instances of `aid=PLACEHOLDER` with your actual ID
- [ ] Test affiliate links to verify tracking works

**Files to update** (search for "PLACEHOLDER"):
- All 7 destination HTML files in `destinations/`
- Use find & replace in your code editor

**Time estimate**: 30 minutes setup + wait for approval

---

### 3. Add Google Analytics
**Status**: 🔴 NOT STARTED

Track your traffic from day one to measure success.

**Action Items:**
- [ ] Create Google Analytics 4 account (analytics.google.com)
- [ ] Get your tracking code (starts with `G-`)
- [ ] Add tracking code to `<head>` section of:
  - `index.html`
  - All 7 destination pages
  - `gift-guides/index.html`
  - `reviews/index.html`
  - `404.html`

**Tracking code to add:**
```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

**Time estimate**: 15 minutes

---

## IMPORTANT - Should Do Before Launch

### 4. Choose Hosting & Deploy
**Status**: 🔴 NOT STARTED

**Recommended Option: Netlify (Easiest)**
- [ ] Create account at netlify.com
- [ ] Drag & drop your `pickleball-website` folder
- [ ] Get free SSL certificate automatically
- [ ] Note your temporary URL (e.g., `random-name.netlify.app`)

**Alternative: GitHub Pages**
- [ ] Create GitHub repository
- [ ] Push code to GitHub
- [ ] Enable GitHub Pages in settings
- [ ] Site will be at `yourusername.github.io/pickleball-website`

**Time estimate**: 30 minutes

---

### 5. Register Domain
**Status**: 🔴 NOT STARTED

**Action Items:**
- [ ] Check if `pickleballaddicts.com` is available
- [ ] Register domain (Namecheap, Google Domains, Cloudflare)
- [ ] Point domain to hosting (Netlify/GitHub Pages)
- [ ] Wait for DNS propagation (up to 48 hours)

**Cost**: $10-15/year

**Time estimate**: 20 minutes + DNS wait time

---

### 6. Create Essential Legal Pages
**Status**: 🔴 NOT STARTED

Required for affiliate compliance and user trust.

**Action Items:**
- [ ] Create `privacy-policy.html` (use free template generator)
- [ ] Create `terms-of-service.html`
- [ ] Add links to footer of all pages
- [ ] Ensure affiliate disclosures are visible (✅ already done)

**Free template generators:**
- termsfeed.com
- privacypolicies.com
- getterms.io

**Time estimate**: 30 minutes

---

## OPTIONAL - Can Do After Launch

### 7. Submit to Google Search Console
**Status**: ⚪ WAITING (do after launch)

**Action Items:**
- [ ] Add site to Google Search Console
- [ ] Verify domain ownership
- [ ] Submit sitemap (create simple XML sitemap)
- [ ] Request indexing for homepage

**Time estimate**: 15 minutes

---

### 8. Create Social Media Presence
**Status**: ⚪ OPTIONAL

**Action Items:**
- [ ] Create Instagram account (@pickleballaddicts)
- [ ] Create Pinterest account (good for travel content)
- [ ] Create Facebook page
- [ ] Share destination content

**Time estimate**: 1-2 hours

---

### 9. Set Up Email Newsletter
**Status**: ⚪ FUTURE (mentioned as "coming soon")

**Action Items:**
- [ ] Sign up for Mailchimp (free tier)
- [ ] Create signup form
- [ ] Add to homepage
- [ ] Create welcome email sequence

**Time estimate**: 1-2 hours

---

## Testing Before Going Live

### Pre-Launch Testing Checklist
**Status**: 🔴 NOT STARTED

**Action Items:**
- [ ] Open every page in browser and verify:
  - [ ] Homepage loads correctly
  - [ ] All 7 destination pages load
  - [ ] Navigation links work
  - [ ] Footer links work
  - [ ] Images display (once added)
  - [ ] Mobile responsive on phone
  - [ ] No console errors (F12 > Console)

- [ ] Test affiliate links:
  - [ ] Click a "Book Now" button
  - [ ] Verify it opens Booking.com
  - [ ] Check URL contains your affiliate ID

- [ ] Test on multiple devices:
  - [ ] Desktop/laptop
  - [ ] Mobile phone
  - [ ] Tablet (if available)

**Time estimate**: 30 minutes

---

## Quick Reference

### Files That Need Updates:

1. **Images needed**: `images/destinations/*.jpg` (7 files)
2. **Affiliate IDs**: All `.html` files in `destinations/` folder
3. **Analytics**: All `.html` files (add tracking code)
4. **Legal pages**: Create `privacy-policy.html` and `terms-of-service.html`

### Estimated Time to Launch:
- **Minimum** (with images ready): 2-3 hours
- **Complete** (including waiting for approvals): 2-3 days
- **Professional** (all optional items): 1 week

---

## Launch Day Checklist

When everything above is complete:

- [ ] Final review of all pages
- [ ] Verify affiliate links have your ID
- [ ] Test on mobile device one more time
- [ ] Announce on social media (if set up)
- [ ] Monitor Google Analytics for first visitors
- [ ] Check Search Console for crawl errors (after 24 hours)

---

## Post-Launch First Week

- [ ] Monitor traffic daily
- [ ] Check for any broken links
- [ ] Verify affiliate tracking works
- [ ] Look for any user-reported issues
- [ ] Start creating content for gift guides section

---

## Priority Order

If you want to launch ASAP, do these in order:

1. **Add images** (1-2 hours) - Site won't look good without them
2. **Set up Booking.com affiliate** (30 min + approval wait)
3. **Update affiliate links** (15 minutes)
4. **Add Google Analytics** (15 minutes)
5. **Deploy to Netlify** (30 minutes)
6. **Test everything** (30 minutes)
7. **Register domain** (20 minutes)
8. **Create legal pages** (30 minutes)
9. **Go live!** 🎉

**Total active time**: ~4 hours
**Total calendar time**: 2-3 days (waiting for approvals)

---

**Good luck with your launch! 🎾**

Remember: It's better to launch with good images and working affiliate links than to wait for perfection. You can always improve content, add features, and optimize after launch.
