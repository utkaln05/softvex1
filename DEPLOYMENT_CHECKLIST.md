# Vercel Deployment Checklist ✅

## Pre-Deployment
- ✅ Project pushed to GitHub (utkaln05/softvex1)
- ✅ vercel.json created with proper configuration
- ✅ .vercelignore file created
- ✅ Environment variables documented
- ✅ Build script working locally (`npm run build`)
- ✅ All forms working with loading states
- ✅ Google Sheets integration tested
- ✅ Email notifications tested
- ✅ Animation optimizations applied
- ✅ Next.js favicon removed

## Environment Variables Required

Add these in Vercel dashboard → Settings → Environment Variables:

| Variable | Value | Source |
|----------|-------|--------|
| GOOGLE_SERVICE_ACCOUNT_EMAIL | website-form-handler@softvex-info.iam.gserviceaccount.com | From .env.local |
| GOOGLE_PRIVATE_KEY | (full private key) | From .env.local |
| GOOGLE_SHEET_ID | 1-wjQoAVgqNKQw-dYM0IIYajlNUC_UhTCeaAUwjTQICA | From .env.local |
| EMAIL_HOST | smtp.zoho.in | From .env.local |
| EMAIL_PORT | 587 | From .env.local |
| EMAIL_SECURE | false | From .env.local |
| EMAIL_USER | info@softvex.in | From .env.local |
| EMAIL_PASS | Czvx05d6bAMU | From .env.local |
| EMAIL_TO | info@softvex.in | From .env.local |

## Deployment Steps

1. **Go to vercel.com** and login
2. **Import project** from GitHub (utkaln05/softvex1)
3. **Add environment variables** (see table above)
4. **Click Deploy** - Wait 2-3 minutes for first build
5. **Get your deployment URL** (e.g., https://softvex-ui.vercel.app)

## Post-Deployment Testing

### Form Testing
- [ ] Visit `/contact` and submit form
- [ ] Visit `/careers` and submit form
- [ ] Verify success toast messages appear
- [ ] Check Google Sheets for new entries
- [ ] Check email (info@softvex.in) for notifications

### Performance Testing
- [ ] Check Vercel Analytics dashboard
- [ ] Verify page load times < 2s
- [ ] Test on mobile devices
- [ ] Verify loading spinners show on form submit

### Functionality Testing
- [ ] Navigation links work
- [ ] All pages load properly
- [ ] Images load correctly
- [ ] Animations run smoothly
- [ ] Forms validate input correctly

## Domain Setup (Optional)

1. In Vercel dashboard → Settings → Domains
2. Add your custom domain (softvex.in)
3. Update DNS records with Vercel nameservers
4. Wait 24-48 hours for propagation

## Monitoring

- Monitor builds: Vercel Dashboard → Deployments
- Check logs: Click on deployment → Logs
- Monitor uptime: Vercel Analytics
- Set up Slack notifications (optional)

## Rollback Plan

If deployment has issues:
1. Go to Deployments
2. Click previous stable deployment
3. Click Promote to Production
4. Investigate issue and refix

## Production Optimization Features

✅ Already enabled:
- Next.js Turbopack for fast builds
- Image optimization
- Code splitting
- Server actions for forms
- Non-blocking email sending
- Optimized animations
- 60-second API timeout

## Next Steps

1. Deploy to Vercel (follow deployment steps above)
2. Configure custom domain
3. Set up SSL/TLS (automatic with Vercel)
4. Monitor performance in first week
5. Collect user feedback

---

**Ready to Deploy:** ✅ YES
**Last Updated:** January 9, 2026
