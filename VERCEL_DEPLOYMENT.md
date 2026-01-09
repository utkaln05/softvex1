# Vercel Deployment Guide - Softvex UI

## Prerequisites
- GitHub account with the project pushed (already done: https://github.com/utkaln05/softvex1)
- Vercel account (free tier available)

## Step-by-Step Deployment

### 1. Connect to Vercel

1. Go to [vercel.com](https://vercel.com) and sign up/login
2. Click "Add New..." → "Project"
3. Select "Import Git Repository"
4. Select your GitHub repository: `utkaln05/softvex1`
5. Click "Import"

### 2. Configure Environment Variables

In the Vercel dashboard, go to **Settings** → **Environment Variables** and add:

```
GOOGLE_SERVICE_ACCOUNT_EMAIL = website-form-handler@softvex-info.iam.gserviceaccount.com
GOOGLE_PRIVATE_KEY = (paste your full private key from .env.local)
GOOGLE_SHEET_ID = 1-wjQoAVgqNKQw-dYM0IIYajlNUC_UhTCeaAUwjTQICA
EMAIL_HOST = smtp.zoho.in
EMAIL_PORT = 587
EMAIL_SECURE = false
EMAIL_USER = info@softvex.in
EMAIL_PASS = Czvx05d6bAMU
EMAIL_TO = info@softvex.in
```

**Important:** Make sure the `GOOGLE_PRIVATE_KEY` includes the full key with all newlines intact.

### 3. Build Settings

Vercel automatically detects Next.js and uses:
- **Build Command:** `npm run build`
- **Output Directory:** `.next`
- **Install Command:** `npm install`

These are already configured in `vercel.json`.

### 4. Deploy

1. Click "Deploy" button
2. Wait for build to complete (should take 2-3 minutes)
3. Once deployed, you'll get a URL like: `https://softvex-ui.vercel.app`

### 5. Connect Custom Domain (Optional)

1. Go to **Settings** → **Domains**
2. Add your custom domain (e.g., softvex.in)
3. Update DNS records with Vercel's nameservers
4. Wait for DNS propagation (can take 24-48 hours)

## Production Environment Features

✅ **Optimizations enabled:**
- Automatic image optimization
- Code splitting and compression
- Fast rebuild times with Turbopack
- API routes with 60-second timeout
- Environmental variables configured

## Testing After Deployment

1. **Contact Form:** Visit `/contact` and submit a test form
2. **Career Form:** Visit `/careers` and submit a test application
3. **Verify Emails:** Check info@softvex.in for notifications
4. **Check Google Sheets:** Verify data is saved to the sheet

## Monitoring & Logs

Monitor your deployment:
1. Go to **Deployments** tab in Vercel
2. Click on the latest deployment
3. View build logs and runtime logs
4. Check analytics for traffic

## Rollback

If something goes wrong:
1. Go to **Deployments**
2. Click on a previous successful deployment
3. Click "Promote to Production"

## Troubleshooting

**Issue:** Form submissions fail
- Check environment variables are set correctly
- Verify Google Sheets service account has access
- Check Zoho mail credentials

**Issue:** Build fails
- Check Node version (Vercel uses Node 18+ by default)
- Run `npm run build` locally to debug
- Check for TypeScript errors

**Issue:** Slow deployments
- This is normal for first build
- Subsequent deployments are faster due to caching
- Check build logs for any warnings

## Update & Redeploy

To update your deployment:
1. Make changes locally
2. Test with `npm run dev`
3. Commit and push to GitHub:
   ```bash
   git add .
   git commit -m "Your message"
   git push origin main
   ```
4. Vercel automatically rebuilds and redeploys

---

**Deployment Status:** Ready to deploy ✅
**Last Updated:** January 9, 2026
