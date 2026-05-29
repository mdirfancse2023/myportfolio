# Deploy to Vercel in 2 Minutes

Your portfolio can be deployed to Vercel immediately (free tier available).

## Step 1: Install Vercel CLI

```bash
npm install -g vercel
```

## Step 2: Login to Vercel

```bash
vercel login
```

This opens your browser to authorize with GitHub.

## Step 3: Deploy

```bash
# From your project root
vercel --prod
```

Vercel will:
1. ✅ Detect it's a Vite app
2. ✅ Build automatically
3. ✅ Deploy to global CDN
4. ✅ Give you a live URL

## Step 4 (Optional): Set Environment Variables

If needed for production:

```bash
vercel env add VITE_SUPABASE_URL
vercel env add VITE_SUPABASE_PUBLISHABLE_KEY
vercel env add OPENROUTER_API_KEY
```

## Auto-Deploy Setup (Optional)

For automatic deploys on every push to main:

1. Go to [vercel.com](https://vercel.com)
2. Connect your GitHub repo
3. Vercel auto-deploys on push

## Your Deployment URLs

After deployment:
- **Live**: `https://myportfolio-xxx.vercel.app`
- **Dashboard**: `https://vercel.com/dashboard`
- **Custom Domain** (optional): Add in Vercel dashboard

## Cost

- **Free tier**: ✅ Perfect for your portfolio
  - Unlimited deploys
  - Global CDN
  - SSL certificate included
  - Custom domains available

---

**That's it!** Your portfolio is live in <2 minutes.

For the current Azure deployment setup, use: `.azure/README.md`
